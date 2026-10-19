# CodeInspector

### A Clean Code Evaluator for Student Python Projects

CodeInspector is a semester project for **Software Construction and Development** at **IMSciences**, under **Engr. Muhammad Umer Haroon**. It aims to help students review the structure, readability, and completeness of their Python projects through configurable static analysis.

**Current status:** Project initiation and requirements planning. This repository currently contains the assignment brief and project proposal. The analyzer has not been implemented yet; the features below describe the planned scope.

## The Problem

A Python project can produce the expected output while still containing large functions, unclear names, repeated code, or incomplete documentation. Reviewing these issues manually takes time, and students benefit from specific feedback they can use to improve their work.

CodeInspector will inspect Python source files and report potential issues with file paths, line numbers where applicable, and improvement suggestions based on the clean code practices covered in the course.

## Objectives and Intended Users

- Help students identify opportunities to improve code readability and structure.
- Support instructors in reviewing selected course rules consistently.
- Highlight project completeness issues, such as missing documentation and test files.
- Provide configurable checks so limits can reflect course expectations.
- Produce understandable findings and transparent scores that guide manual review.

The intended users are students developing Python projects and instructors reviewing those projects.

## Planned Features

| Area | Planned checks | Priority |
| --- | --- | --- |
| Naming | Flag very short or generic identifiers; explore heuristic checks for verb-based function names. | Phase 1 |
| Project completeness | Detect a missing README, missing test files, empty functions, and unused imports. | Phase 1 |
| Reporting | Present findings with locations and suggestions, followed by category scores. | Phase 1 |
| Function structure | Check function length, nesting depth, argument count, return patterns, and recursion, including tail-call patterns where feasible. | Phase 2 |
| Configuration | Allow check thresholds to be changed and individual rules to be enabled or disabled. | Introduced in Phase 1; extended in Phase 2 |
| Duplicate code | Identify functions with similar bodies. | Phase 3, if time permits |
| Experimental style signals | Explore a rough AI-use estimate based on style signals, with explicit limitations. | Optional; subject to review |
| Overall score | Combine category scores using a documented scoring method. | Phase 3, if time permits |

These are initial requirements and may evolve during development. A potential issue reported by a rule is a prompt for review, not proof of a defect.

## How It Will Work

1. The user supplies the path to a Python project folder.
2. CodeInspector discovers Python source files and reads their contents.
3. Python's built-in `ast` module parses source files into abstract syntax trees.
4. Separate rule modules inspect the code structure and record findings.
5. A reporting component combines the findings into readable feedback and scores.

The analyzer will read the submitted source code without executing or importing it. Configuration will control supported thresholds, such as maximum function length and argument count.

## Scope and Limitations

- **Python only:** Other programming languages are outside the initial scope.
- **Static analysis only:** The tool cannot establish that a program runs correctly or meets its intended business requirements.
- **Course-based rules:** Checks represent selected course guidelines. Rules about return counts, recursion, or argument counts may need different settings for different projects.
- **Heuristic findings:** Naming, unused-import, and similarity checks can produce false positives or miss issues, particularly with dynamic Python features.
- **Completeness indicators:** The presence of a README or test files does not establish documentation quality, test coverage, or correctness.
- **Authorship limitations:** Any experimental AI-use estimate would be speculative and must not be treated as proof of authorship or academic misconduct.
- **Local project review:** Cross-project plagiarism detection and comparisons across teams are outside the scope.
- **Scores are guidance:** A combined score is not a certification of software quality or industry readiness.

## Initial Product Backlog

The checklist tracks planned work; unchecked items are not implemented.

- [ ] Prepare the lightweight requirements document and commit the submission copy.
- [ ] Confirm group membership and assign initial responsibilities.
- [ ] Define finding fields, rule identifiers, and reporting conventions.
- [ ] Implement project-folder input and Python file discovery.
- [ ] Add AST parsing with useful handling of syntax errors and unreadable files.
- [ ] Implement initial naming and completeness checks.
- [ ] Add configuration for supported rules and thresholds.
- [ ] Produce a readable report with finding locations and suggestions.
- [ ] Define and document category scoring.
- [ ] Add sample projects and automated tests for the implemented checks.
- [ ] Implement function structure checks.
- [ ] Evaluate duplicate-code detection if time permits.
- [ ] Review the feasibility and usefulness of optional experimental features.
- [ ] Document installation and usage once the analyzer is runnable.

## Repository Contents

```text
CodeInspector/
|-- README.md                         # Project overview, scope, backlog, and workflow
|-- Assignment_1_SCD_IMSCIENCES.pdf    # Assignment instructions
`-- CodeInspector_Project_Proposal.pdf # Initial project proposal
```

As implementation begins, the planned structure is:

```text
src/codeinspector/   # Analyzer, rule modules, configuration, and reporting
tests/              # Automated tests and small analysis fixtures
docs/               # Requirements, design notes, and submission documents
examples/           # Sample inputs and example reports
```

The planned directories will be added when they contain relevant files. The project proposal is an initial concept document; the assignment's lightweight requirements document is still pending.

## Project Member and Responsibilities

| Member | Current responsibility |
| --- | --- |
| Abdul Samad | Project initiation, proposal preparation, and repository setup |

Additional group members and their responsibilities will be recorded once confirmed. Assignment 1 requires a group unless the instructor has approved individual work. This repository does not yet record an individual-work approval.

## Collaboration and Versioning

Repository: [abdulsamad-codes/CodeInspector](https://github.com/abdulsamad-codes/CodeInspector)

- Each member should contribute through their own GitHub account using meaningful commits.
- Keep changes focused and use descriptive commit messages, such as `docs: add initial requirements` or `feat: add function length check`.
- Use short, descriptive branch names, such as `feature/naming-checks`, `fix/parser-errors`, or `docs/requirements`.
- Review changes before merging them into the default branch.
- Update requirements and backlog items as scope and implementation evolve.
- Use lowercase `snake_case` for Python modules and follow Python naming conventions in source code. Use descriptive, consistent names for documentation files.
- Use Git history for revisions instead of creating numbered copies of the same file.
- Use semantic version tags for significant milestones, such as `v0.1.0` for an initial usable development version and `v1.0.0` for the first complete release. No release is claimed by this README.

All members should understand their contributions and be able to explain the project during a review or viva.

## Getting Started

The repository is currently in the planning stage. There is no executable analyzer, installation procedure, or command-line interface yet.

For now, read the project proposal for the initial concept and the assignment brief for submission requirements. Setup instructions, supported Python versions, dependencies, configuration examples, and runnable commands will be added alongside the implementation.

## Assignment 1 Deliverables

- [ ] Verify that the GitHub repository is public and accessible without requesting permission.
- [ ] Confirm collaborators and meaningful contributions from each group member, or record instructor-approved individual work.
- [ ] Complete a lightweight requirements document covering member details, the problem, objectives, intended users, functional and relevant non-functional requirements, priorities, assumptions, constraints, and limitations.
- [ ] Include the requirements document in the repository and submit the same document as a PDF or another instructor-approved format.
- [ ] Maintain a clear repository structure, README, backlog, responsibilities, and traceable Git history.
- [ ] Submit the public repository link and requirements document through the designated group member.

This README supports project organization and provides an overview. The separate requirements submission remains part of the assignment.
