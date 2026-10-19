# CodeInspector

A clean code evaluator for student Python projects.

This is my semester project for Software Construction and Development at IMSciences, taught by Engr. Muhammad Umer Haroon. It will read a Python project and suggest improvements to its naming, formatting, functions, and missing documentation.

**Current status:** Assignment 1 documents are prepared. The analyzer is planned; implementation has not started.

## About Me

Abdul Samad | BSSE, Group A | Semester 5 | Roll number 2

GitHub: [abdulsamad-codes](https://github.com/abdulsamad-codes)

I am working individually with the instructor's permission and will handle development, testing, documentation, and Git updates.

## What It Will Check

- Selected PEP 8 naming and formatting rules, as suggested by Sir Umer.
- Course rules about small functions, nesting, arguments, returns, and recursion.
- Missing README/test files and empty functions.
- Unused imports, similar functions, and scores in a later stage.

AI-use detection is also a research goal for later. It cannot prove who wrote a piece of code.

The tool will run locally from the command line. It will use Python's `ast` module for code structure and text/token checks for formatting, without executing the project's code. Reports will show issues, file locations, and suggestions. Supported rules and limits will be configurable.

## Project Files

- [Requirements](docs/requirements.md) and [submission PDF](docs/requirements.pdf)
- [Task backlog](docs/backlog.md)
- [Version history](CHANGELOG.md)
- Original [assignment](docs/references/Assignment_1_SCD_IMSCIENCES.pdf) and [proposal](docs/references/CodeInspector_Project_Proposal.pdf) in `docs/references/`

```text
CodeInspector/
|-- .gitignore
|-- README.md
|-- CHANGELOG.md
`-- docs/
    |-- requirements.md
    |-- requirements.pdf
    |-- backlog.md
    `-- references/
        |-- Assignment_1_SCD_IMSCIENCES.pdf
        `-- CodeInspector_Project_Proposal.pdf
```

Application code and tests will be added when development begins.

## Naming and Versions

Use descriptive `snake_case` names for functions, variables, and modules, `CapWords` for classes, and `UPPER_SNAKE_CASE` for constants. Folders and ordinary documents use lowercase names; standard files such as README.md keep their usual names.

Work will be recorded directly on `main` in focused commits after checking each change. Commit messages will describe the actual change, for example `docs: clarify requirements` or `feat: check function names`.

Significant milestones use annotated `vMAJOR.MINOR.PATCH` tags: major for incompatible changes after the stable release, minor for features, and patch for fixes. During early 0.x development, interfaces may change. Git history replaces numbered copies of files. Routine wording edits do not need a new tag.

`v0.1.0` marks the initial planning work. `v1.0.0` will mark the first complete version. The requirements and backlog will be updated during the semester.

These checks provide feedback, not proof of program correctness or complete PEP 8 compliance.

## Assignment 1 Submission

Review the requirements, then submit this public repository link and [docs/requirements.pdf](docs/requirements.pdf). The PDF is the same document kept in the repository. Requirements, responsibilities, and progress will continue to be updated during the semester.

Repository: [CodeInspector](https://github.com/abdulsamad-codes/CodeInspector)

Reference: [PEP 8](https://peps.python.org/pep-0008/)
