# CodeInspector

### A Clean Code Evaluator for Student Python Projects

CodeInspector is my semester project for Software Construction and Development at IMSciences, taught by Engr. Muhammad Umer Haroon. It will inspect Python projects and give feedback about naming, code style, function structure, and project completeness.

**Status:** Requirements and project planning. The analyzer has not been implemented yet.

## Project Member

| Detail | Information |
| --- | --- |
| Name | Abdul Samad |
| Program | BSSE, Group A, Semester 5 |
| Roll number | 2 |
| GitHub | [abdulsamad-codes](https://github.com/abdulsamad-codes) |
| Working arrangement | Individual project, with instructor permission |

I am responsible for requirements, implementation, testing, documentation, and maintaining the Git repository.

## Why This Project?

Students can write programs that work but still have unclear names, large functions, repeated code, or missing documentation. CodeInspector will point out selected issues with their file locations and suggestions for improvement. It is intended for students reviewing Python projects and instructors providing feedback.

## Planned Checks

The checks will come from two main sources:

- **PEP 8:** Python naming and formatting guidance. Sir Umer recommended researching it when reviewing the project idea. The selected checks and their limits are listed in the [requirements](docs/requirements.md).
- **Course slides:** Meaningful names, small focused functions, shallow nesting, argument counts, return patterns, and recursion review.

Other planned checks include missing README/test files, empty functions, unused imports, and duplicate function bodies. The report will explain findings and, later, show scores with a documented calculation.

AI-use detection remains a later research goal. It will be explored after the core rules work. Style signals alone cannot prove who wrote code, so any experimental result must clearly state its limitations.

## How It Will Work

1. The user gives the path to a Python project folder.
2. CodeInspector reads its Python files without running or importing them.
3. Python's `ast` module checks code structure; source text and tokens support formatting checks.
4. Separate checks record findings with rule names, file paths, line numbers where applicable, and suggestions.
5. A report presents the results. Settings will allow supported rules and limits to be changed.

The first interface will be a local command-line tool. No web application or database is planned for the initial version.

## Documents and Folder Structure

```text
CodeInspector/
|-- .gitignore
|-- README.md
|-- CHANGELOG.md
|-- Assignment_1_SCD_IMSCIENCES.pdf
|-- CodeInspector_Project_Proposal.pdf
`-- docs/
    |-- requirements.md
    |-- requirements.pdf
    `-- backlog.md
```

- [Requirements](docs/requirements.md): project details, functional/non-functional requirements, priorities, assumptions, and limitations.
- [Requirements PDF](docs/requirements.pdf): submission copy of the requirements document.
- [Backlog](docs/backlog.md): planned tasks, responsibilities, and progress.
- [Changelog](CHANGELOG.md): significant project milestones.

As implementation starts, `codeinspector/` will hold application modules and `tests/` will hold tests. These folders will be added when they contain actual work.

## Naming and Git Conventions

- Use descriptive `snake_case` for Python modules, functions, and variables; `CapWords` for classes; and `UPPER_SNAKE_CASE` for constants.
- Use lowercase descriptive names for folders and ordinary documents, keeping conventional names such as `README.md` and `CHANGELOG.md`.
- Preserve the supplied assignment/proposal filenames.
- Keep functions focused and follow the selected PEP 8 and course guidance.
- Make focused commits with meaningful messages describing actual changes.
- Maintain versions through Git history and annotated tags rather than duplicate files such as `final_v2.py`.
- Use `vMAJOR.MINOR.PATCH`: major for incompatible changes after the stable release, minor for features, and patch for fixes. During initial `0.x` development, interfaces may change and will be documented.
- `v0.1.0` identifies the requirements/planning baseline; it does not claim a working analyzer. Later milestones will be tagged when implemented and checked. `v1.0.0` will identify the first complete agreed version.

## Limitations

The tool will check selected style and structure rules, not program correctness. Naming and similarity findings need human review. Finding test files does not prove coverage. PEP 8 guidance and course-specific rules will be identified separately; this project does not claim complete PEP 8 compliance checking. Scores will summarize configured checks rather than certify overall software quality.

## Assignment 1

The requirements document, responsibilities, backlog, naming conventions, and version record are included here. Before submission, I still need to review the documents, verify public access to the repository and its committed PDF, and submit the repository link and that same PDF.

Repository: [CodeInspector](https://github.com/abdulsamad-codes/CodeInspector)

Reference: [PEP 8 - Style Guide for Python Code](https://peps.python.org/pep-0008/)
