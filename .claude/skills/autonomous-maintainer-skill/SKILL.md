```markdown
# autonomous-maintainer-skill Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill demonstrates best practices for maintaining and contributing to the `autonomous-maintainer-skill` Python codebase. It covers the project's coding conventions, file organization, commit patterns, and testing approaches. By following these guidelines, contributors can ensure consistency, readability, and maintainability across the repository.

## Coding Conventions

### File Naming
- **Convention:** PascalCase is used for file names.
- **Example:**  
  ```
  AutonomousMaintainer.py
  SkillManager.py
  ```

### Import Style
- **Convention:** Use relative imports within the package.
- **Example:**
  ```python
  from .SkillManager import SkillManager
  from .utils import helper_function
  ```

### Export Style
- **Convention:** Named exports are preferred.
- **Example:**
  ```python
  class AutonomousMaintainer:
      pass

  def helper_function():
      pass
  ```

### Commit Patterns
- **Type:** Freeform messages (no strict prefix required)
- **Average Length:** 42 characters
- **Example:**
  ```
  Improve error handling in SkillManager
  Add logging to AutonomousMaintainer
  ```

## Workflows

### Adding a New Skill
**Trigger:** When you want to introduce a new skill module to the codebase  
**Command:** `/add-skill`

1. Create a new Python file using PascalCase (e.g., `NewSkill.py`).
2. Implement the skill logic, using named exports.
3. Use relative imports to reference other modules.
4. Write corresponding test files following the `*.test.*` pattern.
5. Commit changes with a clear, concise message.

### Updating an Existing Skill
**Trigger:** When modifying or improving an existing skill  
**Command:** `/update-skill`

1. Locate the relevant skill file (e.g., `SkillManager.py`).
2. Make necessary changes, maintaining code style conventions.
3. Update or add tests as needed.
4. Commit with a descriptive message summarizing the update.

### Running Tests
**Trigger:** To verify code correctness after changes  
**Command:** `/run-tests`

1. Identify all test files matching the `*.test.*` pattern.
2. Run tests using the project's preferred method (framework unknown; use standard Python test runners if unsure).
3. Review test output and address any failures.

## Testing Patterns

- **File Pattern:** Test files are named using the `*.test.*` convention (e.g., `SkillManager.test.py`).
- **Framework:** Not specified; use standard Python testing frameworks such as `unittest` or `pytest` if needed.
- **Example:**
  ```python
  # SkillManager.test.py
  import unittest
  from .SkillManager import SkillManager

  class TestSkillManager(unittest.TestCase):
      def test_initialization(self):
          manager = SkillManager()
          self.assertIsNotNone(manager)
  ```

## Commands
| Command         | Purpose                                             |
|-----------------|-----------------------------------------------------|
| /add-skill      | Scaffold and add a new skill module                 |
| /update-skill   | Update or refactor an existing skill module         |
| /run-tests      | Execute all tests in the repository                 |
```
