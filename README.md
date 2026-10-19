# CodeInspector

A clean code evaluator for student Python projects.

This is my semester project for Software Construction and Development at IMSciences, taught by Engr. Muhammad Umer Haroon. It will read a Python project and suggest improvements to its naming, formatting, functions, and missing documentation.

**Current status:** Planning and requirements are prepared. Development has not started.

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
- Original assignment and proposal PDFs in the root folder

Application code and tests will be added when development begins.

## Naming and Versions

Use descriptive `snake_case` names for functions, variables, and modules, `CapWords` for classes, and `UPPER_SNAKE_CASE` for constants. Folders and ordinary documents use lowercase names; standard files such as README.md keep their usual names.

Changes will have meaningful commits. Significant milestones use annotated `vMAJOR.MINOR.PATCH` tags: major for incompatible changes after the stable release, minor for features, and patch for fixes. During early 0.x development, interfaces may change. Git history replaces numbered copies of files.

`v0.1.0` marks the initial planning work. `v1.0.0` will mark the first complete version. The requirements and backlog will be updated during the semester.

These checks provide feedback, not proof of program correctness or complete PEP 8 compliance. Before submitting Assignment 1, I need to review the documents and submit the public repository link with the committed PDF.

Repository: [CodeInspector](https://github.com/abdulsamad-codes/CodeInspector)

Reference: [PEP 8](https://peps.python.org/pep-0008/)
