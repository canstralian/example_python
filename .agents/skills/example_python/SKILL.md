```markdown
# example_python Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and workflows used in the `example_python` repository. The codebase is written in Python and does not use a specific framework. It emphasizes consistent file naming, import/export styles, and includes a workflow for bulk updating dependencies across multiple subprojects.

## Coding Conventions

### File Naming
- Use **snake_case** for all file names.
  - Example: `my_module.py`, `data_processor.py`

### Import Style
- Use **relative imports** within the package.
  - Example:
    ```python
    from .utils import helper_function
    ```

### Export Style
- Use **named exports** (explicitly listing what is exported).
  - Example:
    ```python
    __all__ = ["MyClass", "my_function"]
    ```

### Commit Patterns
- Commit messages are freeform, generally concise (~56 characters).
  - Example: `fix: handle edge case in data parsing`

## Workflows

### Bulk Dependency Update (pip)
**Trigger:** When dependencies need to be updated in multiple Python subprojects at once.  
**Command:** `/update-dependencies pip`

1. Identify outdated dependencies across all subprojects.
2. Update dependency versions in each subproject's `requirements.txt` and/or `pyproject.toml`.
3. Commit all updated dependency files together.

**Files involved:**
- `**/requirements.txt`
- `**/pyproject.toml`

**Example:**
```shell
# Update dependencies in all subprojects
/update-dependencies pip
```

## Testing Patterns

- **Framework:** Unknown (not explicitly detected)
- **File Pattern:** Test files follow the `*.test.*` naming convention.
  - Example: `math_utils.test.py`, `api_handler.test.py`
- Tests are likely colocated with the modules they test.

## Commands

| Command                  | Purpose                                                        |
|--------------------------|----------------------------------------------------------------|
| /update-dependencies pip | Bulk update Python dependencies across all subprojects         |
```
