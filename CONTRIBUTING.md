# Contributing

Thank you for your interest in contributing! This document provides guidelines and instructions for contributing to this project.

## Code of Conduct

- Be respectful and inclusive
- Focus on constructive feedback
- Help make the community welcoming for everyone

## Getting Started

### Prerequisites

- Python 3.10+ (or C++20 for LOB engines)
- Git for version control
- Familiarity with the project's tech stack

### Setup Development Environment

1. **Fork and Clone**
   ```bash
   git clone https://github.com/YOUR_USERNAME/REPO_NAME.git
   cd REPO_NAME
   ```

2. **Install Dependencies**
   ```bash
   # Python projects
   pip install -e ".[dev]"

   # C++ projects
   mkdir build && cd build
   cmake .. && make
   ```

3. **Install Pre-commit Hooks**
   ```bash
   pre-commit install
   ```

## Development Workflow

### 1. Create a Branch

```bash
git checkout -b feature/your-feature-name
# or
git checkout -b fix/issue-description
```

Branch naming conventions:
- `feature/` - New features
- `fix/` - Bug fixes
- `docs/` - Documentation updates
- `refactor/` - Code refactoring
- `test/` - Test additions/modifications

### 2. Make Changes

- Write clear, concise commit messages
- Follow existing code style and conventions
- Add tests for new functionality
- Update documentation as needed

### 3. Test Your Changes

```bash
# Python projects
pytest
ruff check .
mypy .

# C++ projects
ctest
clang-tidy src/*.cpp
```

### 4. Commit Your Changes

```bash
git add .
git commit -m "type: brief description

Detailed explanation if needed."
```

Commit message types:
- `feat:` - New feature
- `fix:` - Bug fix
- `docs:` - Documentation only
- `style:` - Formatting, missing semicolons, etc.
- `refactor:` - Code change that neither fixes a bug nor adds a feature
- `test:` - Adding missing tests
- `chore:` - Maintenance tasks

### 5. Push and Create Pull Request

```bash
git push origin feature/your-feature-name
```

Then create a Pull Request on GitHub with:
- Clear title describing the change
- Description of what changed and why
- Reference to related issues (e.g., "Fixes #123")
- Screenshots/examples if applicable

## Code Style Guidelines

### Python

- Follow PEP 8
- Use type hints
- Maximum line length: 120 characters
- Use meaningful variable names
- Document complex logic with comments

### C++

- Follow C++20 best practices
- Use `snake_case` for functions/variables
- Use `PascalCase` for classes
- Prefer `const` and `constexpr` where applicable
- Use smart pointers over raw pointers

### Documentation

- Keep README.md up to date
- Add docstrings to all public functions
- Include usage examples for new features

## Testing

- Write unit tests for all new code
- Ensure all tests pass before submitting PR
- Aim for >80% code coverage
- Include integration tests for complex features

## Reporting Issues

When reporting bugs, include:

1. **Description**: Clear summary of the issue
2. **Steps to Reproduce**: Detailed steps to recreate the problem
3. **Expected Behavior**: What should happen
4. **Actual Behavior**: What actually happens
5. **Environment**: OS, Python/C++ version, relevant dependencies
6. **Logs/Screenshots**: Any relevant error messages or visuals

## Pull Request Process

1. **Before Submitting**
   - Ensure all tests pass
   - Update documentation
   - Rebase on latest main branch
   - Verify pre-commit hooks pass

2. **During Review**
   - Respond to feedback promptly
   - Make requested changes
   - Keep discussion focused and professional

3. **After Approval**
   - Squash commits if requested
   - Maintainer will merge your PR

## Questions?

- Check existing issues and discussions
- Open a new issue with the "question" label
- Reach out to maintainers if needed

## License

By contributing, you agree that your contributions will be licensed under the same license as the project.

---

**Thank you for contributing! 🎉**
