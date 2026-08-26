# Contributing Findings

This repository welcomes documented findings from people who run the Project Aurora synthetic continuity test.

The purpose is not to collect only positive results. Clear failures, contradictions, missing information, semantic drift, and unexpected behaviour are equally valuable.

## How to Contribute

1. Fork this repository.
2. Run or review the Project Aurora test.
3. Copy the result template from:

   `synthetic-test/results/result-template.md`

4. Add your completed result under:

   `synthetic-test/results/`
5. Use a unique result directory or filename.
6. Open a Pull Request against the `main` branch.
7. Explain what was tested and which AI systems, models, or workflow were used.

## Findings Should Distinguish

Please separate:

- observed behaviour;
- interpretation;
- decision;
- limitation;
- unresolved question;
- suggestion for further testing.

Do not present one test as universal proof.

## Recommended Result Structure

A contribution should describe:

- the test setup;
- the source material used;
- the Workstate that was transferred;
- the receiving AI system;
- what the receiving system was asked to do;
- what information was preserved;
- what information was lost or changed;
- any semantic drift;
- any repeated or unnecessary work;
- any authority or provenance problems;
- the contributor’s conclusion;
- remaining uncertainty.

## Do Not Submit

Do not include:

- API keys or passwords;
- private conversations;
- private Memory Banks;
- personal identifiers;
- confidential project material;
- harmful or operationally sensitive information.

Project Aurora is a synthetic test environment. Please keep submitted findings within that scope.

## Pull Request Requirements

Before submitting a Pull Request, confirm that:

- the test setup is clearly documented;
- observed behaviour is separated from interpretation;
- limitations and uncertainty are included;
- private information and secrets have been removed;
- the contribution does not present one result as universal validation;
- the changed files are placed in the correct repository location;
- the contribution follows the existing terminology and structure.

## Review Process

All submissions are reviewed before merging.

A Pull Request may be revised, rejected, or merged with edits if it does not follow the repository scope, evidence requirements, privacy expectations, or documentation standards.

The maintainer may also classify a contribution as:

- exploratory;
- incomplete;
- contradictory;
- unresolved;
- partially relevant;
- accepted finding.

The purpose of review is not to remove criticism. It is to preserve clarity, provenance, evidence, and useful distinctions between different findings.

## Contribution Principle

The Project Aurora test is intended to make the method reviewable by people other than its original creator.

Independent findings, including negative findings, help reveal:

- what the method preserves;
- what it fails to preserve;
- where interpretation becomes uncertain;
- where semantic drift occurs;
- which parts require further development.

Contributions should help make the AI Continuity Architecture Method clearer, more testable, more honest about its limitations, and easier for others to understand.
