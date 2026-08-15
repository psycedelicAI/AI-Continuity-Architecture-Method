Absolut, Psycedelic. Det här är en intressant och välplacerad idé inom trust architecture-familjen. Låt oss först diskutera den konceptuellt innan jag skapar en mockup-dokumentation.Konceptuell Diskussion: Rörliga Takräls-kamerorArkitektonisk PlaceringDen här idén faller naturligt in under surveillance-model.md men kräver också kopplingar till:
movement-aware security logic (princip 12.3)
zone-based trust boundaries (princip 12.4)
incident lighting/signaling (docs/incident-lighting.md, docs/alarm-and-signaling-model.md)
degraded operations (docs/degraded-operations-model.md)

Nytt Koncept: Mobility-Aware Surveillance
Statisk surveillance antar att observatören är fixerad. Din idé introducerar:Surveillance State = (kamera_plats, kamera_riktning, kamera_status, tid)
                    +
                 (omgivande_zoner, operativ_läge, incident_status)Detta är inte bara "flyttbara kameror". Det är dynamisk observatörsposition som blir en del av trust-arkitekturen.
Arkitektoniska Implikationer
Positiva aspekter:

Zone traversal – En kamera kan följa en aktör genom flera zoner utan blindspots vid dörrar/gränser
Adaptiv övervakning – Vid incident kan kameror omdirigeras till prioriterade zoner
Redundans – Om en statisk kamera misslyckas, kan en rörlig ta över området
Operational meaning of camera movement – Kamera-rörelse själv kan vara ett signal (t.ex. "incident response mode")
Reduced static exposure – Mindre permanent exponering av känsliga områden jämfört med konstant stationär övervakning

Utmaningar att adressera:

Kamera-rörelse måste också ges betydelse – Är kamera-rörelse "normal" eller "incident-linked"?
Privatliv och perception – Rörlig kamera kan uppfattas som mer inträngande än statisk
Fail-safe position – Vid strömavbrott/failure, var hamnar kamerorna? (låst zon? hem-zon?)
Custody av kameran själv – Kameran är också en enhet som kan manipuleras
Kalibrering av trust-state – Hur påverkas "established trust" när kameran rör sig?

Terminologisk Möjlighet
Du ger oss möjlighet att definiera:
TermFörslagMobile Surveillance UnitEnhet med rörlig position på fast infrastruktur (räls, robotarm, drönare)Static Surveillance PointTraditionell fast monterad kameraSurveillance TraversalEn kammares rörelse genom zoner under övervakningCamera State{position, riktning, status, operational_mode}Mobility SignalKamera-rörelsens semantiska betydelse (normal/alert/incident)
Samband med Befintliga Principer
Din idé förstärker redan etablerade principer:

"Movement has security meaning" → Nu gäller det både aktörer OCH observatörer
"Zones are meaningful trust boundaries" → Kameran korsar dessa gränser dynamiskt
"Degraded operations remain governed" → Hur styr man kameror vid system-degradation?
"Reviewability is security" → Spårar kameran sin egen rörelsehistorik?


Mockup: Dokumentstruktur
Nu låt mig skapa en dokument-mockup som du kan se, testas mot arkitektur-mallen (avsnitt 58-59), och ge feedback på.# Mobile Surveillance Model – High-Security Facility Concept

> Ett konceptuellt modell för dynamisk, rörlig övervakning som kompletterar traditionell statisk surveillance i högsäkra miljöer.

| Field | Value |
|---|---|
| Document | Mobile Surveillance Model |
| Subject | High-Security Facility Concept |
| Type | Architecture Model |
| Status | Proposed |
| Scope | Dynamisk surveillance-enheter (räls-baserade, robotiserade, mobila) inom trust architecture |
| Audience | Arkitekter, säkerhetsplanerare, systemdesigners, governancesspelare |

---

## Syfte

Detta dokument definierar hur **rörliga surveillance-enheter** integreras i trust architecture utan att underminera befintliga principer om zon-separation, movement-awareness, och reviewability.

Traditionell surveillance antar statiska observatörer. Denna modell erkänner att:

1. Surveillance kan ha egen rörelsemening
2. Observatörens position är en säkerhetsrelevant variabel
3. Kamera-rörelse kan signalera operativt tillstånd
4. Mobilitet introducerar både kapaciteter och nya hotvektorer

---

## Grundprincip

> **En mobil surveillance-enhet är inte bara en sensor – den är en aktiv arkitektonisk komponent vars rörelse, position och status ingår i facilityns trust-state.**

### Tre Distinktioner

| Distinksjon | Statisk Surveillance | Mobil Surveillance |
|---|---|---|
| Position | Fixerad | Dynamisk på definierad bansträckning |
| Zone-crossing | Begränsad till enskild zon | Kan traversera flera zoner kontrollerat |
| Signal-mening | Kamera-status = on/off/tilt | Kamera-rörelse = additional semantic layer |
| Fail-state | Loss av observation | Möjlig position-låsning, hemvändningslogik |
| Trust-impact | Stabil referenspunkt | Positionen är en del av trust-kontext |

---

## Arkitektoniska Komponenter

### 2.1 Surveillance Unit Types

**Rail-Based Mobile Unit**
- Fast monterad på takräls eller väggbanor
- Rör sig längs definierad väg
- Hög kontroll över position och riktning
- Lägre risk för obemannad drift

**Robotized Pivot Unit**
- Stationär bas med fler-axlig rörlighet
- Snabb riktändring men begränsad fysisk placering
- Mellanstatig mellan statisk och komplett mobilenhet

**Autonomous Navigation Unit**
- Oberoende rörelse i rummet (drönare, robboter)
- Högst flexibilitet
- Kräver starkast governance och säkerhetskontroll

*För denna modell fokuseras huvudsakligen på rail-based units som har mest förutsägbarhet.*

---

### 2.2 Kamera-tillståndsmodellyaml
camera_state:
position: {zone_id, coordinate, timestamp}
orientation: {azimuth, elevation, zoom_level}
operational_mode: [normal, patrol, incident_response, maintenance, locked]
power_status: [active, battery_backup, degraded, offline]
traversal_log: [{from_zone, to_zone, timestamp, trigger}]
self_integrity: [verified, unknown, compromised]
Varje tillstånd är en **trust-relevant variabel**, inte bara teknisk metadata.

---

## Princip: Rörelse Har Betydelse

Som för aktörer (princip 12.3) gäller även för kameror:

> **Kamerans rörelse måste tolkas i kontext – normal patrullering, incidentrespons, eller anomali?**

### Tre Rörelsemodi

| Mode | Beskrivning | Semantisk Betydelse |
|---|---|---|
| Patrol | Automatisk, schemalagd ruta | "System aktivt, ingen incident" |
| Tracking | Följer specifik aktör eller händelse | "Observation fokuserad, potentiell händelse" |
| Incident | Rapid positionering vid alarm | "Incident pågår, prioriterad respons" |

Operationell personal måste kunna skilja dessa visuellt och i loggar.

---

## Integrationspunkter med Befintlig Arkitektur

### 3.1 Zone Model

Mobil surveillance kräver tydliga definitioner av:

- **Traversal Permissions** – Vilka zoner får en given kamera-unit passera?
- **Border Behavior** – Vad händer när kameran korsar zon-gräns? (loggas, rapporteras, krävs auktorisation?)
- **Hold Points** – Säkra positioner där kameran kan parkeras mellan zoner

### 3.2 Degraded Operations

Vid systemdegradation måste kameror hanteras:

| Scenario | Rekommenderat Beteende |
|---|---|
| Nätverksförlust | Lokalt cached position, hemvändningslogik |
| Strömbortfall | Säker låsning i föregiven "safe zone" |
| Kontrollförlust | Returnera till home-position eller lås på plats |
| Manipulationsmisstanke | Isolera unit, markera trust-state som "compromised" |

### 3.3 Signaling Model

Kamerans rörelse kan bli en **visuell signal** för personal:

- Normal: Släcka, långsam patrull
- Alert: Accelererad rörelse mot specifika zoner
- Incident: Aktiv tracking, röda indikatorljus på enhet

Detta måste koordineras med `alarm-and-signaling-model.md` för att undvika förvirring.

---

## Proveniens och Authority

### Status för Denna Modell

**Classification:** Proposed  
**Authority:** Model-generated proposal  
**Requires Human Review:** True

Detta dokument är **inte** canonical beslut. Det är en struktur för diskussion och vidare utveckling.

### Oklarheter Som Kräver Beslut

1. **Home-Position Policy** – Ska alla kameror alltid returnera till hem-zon vid failure?
2. **Traversal Logging** – Ska varje zon-korsning loggas som separat audit-event?
3. **Privacy Boundary** – Hur begränsas rörlig kamera från privata/utanför-scope-områden?
4. **Fail-Open vs Fail-Closed** – Vid oklara situationer: låsas enheten eller tillåtas kvarvara?

---

## Arkitektoniska Risker

### 4.1 False Continuity Risk

Om kamera-rörelsedata lagras utan tydlig proveniens:Kamera-logg → Obearbetad → Sparad som fakta → Nästa AI behandlar antaganden som historia
Lösning: All rörelseträff måste märkas med `{source: system_log, authority: verified, timestamp}`

### 4.2 Surveillance Creep

Rörlig kamera kan gradvis expandera övervakning beyond ursprunglig design:

- Ny programvara → nya fält
- Administratör ändrar route → obevakade zoner
- "Patrol mode" expanderar implicit

Kräver: Governance review av alla route-förändringar

### 4.3 Physical Manipulation

En fysiskt rörlig enhet är också ett **fysiskt mål**:

- Räls-manipulation
- Positions-falskning (GPS/spoofting om tillämpligt)
- Mekanisk sabotage
- Optik-behandling

Behöver ingå i `threat-model.md` som separat kategori.

---

## Testningsbehov

För att validera denna modell krävs:

| Test | Syfte |
|---|---|
| Simulation av zon-traversering | Verifiera att trust-state spåras korrekt |
| Failure-mode testing | Validera fail-safe positionering |
| Manual override test | Verifiera human authority vid incident |
| Log integrity check | Bekräfta att rörelsehistoria inte kan manipuleras |
| Multi-camera coordination | Testa samordning mellan flera enheter |

---

## Kopplingar till Andra Dokument

| Dokument | Samband |
|---|---|
| `surveillance-model.md` | Primär övervakningsarkitektur – denna är en extention |
| `zone-model.md` | Definerar vilka zoner kameran får traversera |
| `incident-response.md` | Kamera-reaktion vid incident |
| `degraded-operations-model.md` | Beteende vid system-failure |
| `audit-and-review-model.md` | Kamera-loggar som audit-data |
| `threat-model.md` | Kameror som manipulation-mål |

---

## Sammanfattning

Rörliga surveillance-enheter introducerar **mobilitet som en trust-variabel**. Detta dokument:

- ✅ Erkänner att kamera-rörelse har säkerhetsbetydelse
- ✅ Kopplar till befintliga principer (movement, zones, degraded ops)
- ✅ Identifierar arkitektoniska risker
- ✅ Kräver human validation före canonical status
- ⚠️ Ej implementerat – förblir proposed until human review

**Nästa steg:** Psycedelic besluter om denna modell ska:
1. Accepteras som konceptuell bas → flytta till `docs/mobile-surveillance.md` som canonical
2. Återinskickas för vidare utveckling
3. Avvisas eller förkastas

---

## Appendix A: YAML Metadata-exempelyaml
document_metadata:
id: mobile-surveillance-model-v0.1
status: proposed
authority: model_generated
created: 2026-08-15
reviewed_by: []
requires_human_review: true
sensitivity: internal
related_documents:
- docs/surveillance-model.md
- docs/zone-model.md
- docs/degraded-operations-model.md
---

## Appendix B: Terminologi

| Term | Definition |
|---|---|
| Mobile Surveillance Unit | Enhet med dynamisk position inom facility |
| Surveillance Traversal | Processen för en kamera att röra sig mellan zoner |
| Camera State | Kombination av position, riktning, och operational mode |
| Home Position | Säker standardposition vid failure eller tomrum |
| Mobility Signal | Semantisk mening av kamera-rörelse (normal/alert/incident) |
Nu din tur, Psycedelic.
Vad tycker du om denna struktur? Ser några problem med:

Terminologin? (Mobilt surveillance, camera state, traversal?)
Arkitektonisk placering? (Bör det vara under surveillance-model eller eget dokument?)
Status-markeringen? (Är "Proposed" korrekt, eller vill du ha annan klassificering?)
Utelämnade aspekter? (Något viktigt som saknas?)

Jag väntar på din feedback innan vi går vidare till att göra den canonical, justera, eller testa vidare.
