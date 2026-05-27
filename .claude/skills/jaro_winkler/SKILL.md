```markdown
# jaro_winkler Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the development patterns, coding conventions, and workflows used in the `jaro_winkler` Ruby repository. You'll learn how to contribute code, follow commit and file naming conventions, manage releases, and run or add tests in this codebase.

## Coding Conventions

- **File Naming:**  
  Files use camelCase naming.  
  _Example:_  
  ```
  lib/jaroWinkler.rb
  ```

- **Import Style:**  
  Relative imports are used to reference local files.  
  _Example:_  
  ```ruby
  require_relative 'jaroWinkler'
  ```

- **Export Style:**  
  Named exports are preferred, typically using Ruby module or class exports.  
  _Example:_  
  ```ruby
  module JaroWinkler
    # ...
  end
  ```

- **Commit Patterns:**  
  - Mixed types, with prefixes like `chore`, `feat`, `ci`
  - Average commit message length: 47 characters  
  _Examples:_  
  ```
  chore: update dependencies
  feat: add support for Unicode strings
  ci: fix workflow for Ruby 3.0
  ```

## Workflows

### Version Bump and Changelog Update
**Trigger:** When a new release is prepared following new features or bugfixes  
**Command:** `/bump-version`

1. Update the version number in `lib/jaro_winkler/version.rb`
2. Add or update the relevant entry in `CHANGELOG.md`

_Example:_  
```ruby
# lib/jaro_winkler/version.rb
module JaroWinkler
  VERSION = "1.2.0"
end
```
```markdown
# CHANGELOG.md
## [1.2.0] - 2024-06-01
### Added
- Support for Unicode strings
```

### Merge Pull Request
**Trigger:** When a pull request is approved and merged into the main branch  
**Command:** `/merge-pr`

1. Merge the branch into `main`
2. Include all files changed in the PR (could be code, CI, docs, etc.)

_Example:_  
Files commonly involved:
- `.github/workflows/test.yml`
- `ext/jaro_winkler/extconf.rb`
- `ext/jaro_winkler/jaro.c`
- `README.md`

## Testing Patterns

- **Framework:** Unknown (no explicit test framework detected)
- **Test File Pattern:** Files named with `*.test.*`
- **Typical Test File Example:**  
  ```
  test/stringDistance.test.rb
  ```
- **How to Add Tests:**  
  1. Create a new test file following the `*.test.*` pattern.
  2. Write Ruby test code (framework-agnostic or using your preferred test library).
  3. Place the test file alongside the code it tests or in a dedicated test directory.

## Commands

| Command        | Purpose                                               |
|----------------|-------------------------------------------------------|
| /bump-version  | Bump the gem version and update the changelog         |
| /merge-pr      | Merge an approved pull request into the main branch   |
```
