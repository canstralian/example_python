```markdown
# example_python Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill provides guidance on the development patterns and workflows used in the `example_python` repository. The codebase is written in Python and does not rely on any specific framework. It follows consistent coding conventions and includes automated workflows for dependency management. This document outlines the repository's coding standards, typical workflows, testing patterns, and available automation commands.

## Coding Conventions

### File Naming
- Use **snake_case** for all file and module names.
  - Example: `my_module.py`, `data_processor.py`

### Import Style
- Use **relative imports** within the package.
  - Example:
    ```python
    from .utils import helper_function
    ```

### Export Style
- Use **named exports** (i.e., explicitly define what is exported from a module).
  - Example:
    ```python
    def useful_function():
        pass

    __all__ = ['useful_function']
    ```

### Commit Patterns
- Commit messages are freeform, with no strict prefix requirements.
- Average commit message length is around 56 characters.
- Example:
  ```
  Fix bug in data parsing for edge case inputs
  ```

## Workflows

### Dependency Update (Pip Group)
**Trigger:** When dependencies need to be updated across many Python subprojects at once (e.g., for security, bugfix, or feature updates).
**Command:** `/update-dependencies pip`

1. Identify outdated dependencies in all relevant subproject directories.
2. Update the dependency versions in `requirements.txt` and/or `pyproject.toml` files.
3. Commit all updated files in a single commit, including a detailed changelog in the commit message.

**Files Involved:**
- `**/requirements.txt`
- `**/pyproject.toml`

**Example:**
```bash
/update-dependencies pip
```
This will trigger the batch update process for all pip-managed dependencies.

## Testing Patterns

- **Framework:** Unknown (no standard framework detected).
- **Test File Pattern:** Test files follow the `*.test.*` naming convention.
  - Example: `utils.test.py`, `data_processor.test.py`
- Tests are typically placed alongside the code they test or in dedicated test directories.

## Commands

| Command                  | Purpose                                                      |
|--------------------------|--------------------------------------------------------------|
| /update-dependencies pip | Batch update all pip dependencies across subprojects         |
```
