# Contributing to FusionWrite AI

Thank you for considering contributing to FusionWrite AI! We welcome contributions from the community and are excited to work with you. This document provides guidelines and instructions for contributing to our project.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How to Contribute](#how-to-contribute)
- [Code Standards](#code-standards)
- [Pull Request Process](#pull-request-process)
- [Development Setup](#development-setup)
- [Reporting Issues](#reporting-issues)
- [Getting Help](#getting-help)

## Code of Conduct

Please note that this project is released with a [Contributor Code of Conduct](CODE_OF_CONDUCT.md). By participating in this project, you agree to abide by its terms. We expect all contributors to be respectful and constructive in their interactions.

## How to Contribute

We accept contributions in several forms:

### 1. **Bug Reports and Feature Requests**
- Check existing issues before creating a new one
- Provide a clear description of the issue or feature
- Include relevant code snippets, screenshots, or logs
- Specify your environment (OS, Python version, etc.)

### 2. **Code Contributions**
- Fork the repository
- Create a feature branch from `main`
- Make your changes following our code standards
- Write or update tests as necessary
- Submit a pull request

### 3. **Documentation Improvements**
- Fix typos and improve clarity
- Add examples and use cases
- Update outdated information
- Improve README and other documentation files

### 4. **Testing**
- Write unit tests for new features
- Test bug fixes to prevent regressions
- Run the full test suite before submitting a PR

## Code Standards

We maintain high code quality standards to ensure FusionWrite AI is reliable and maintainable.

### Python Style Guide
- Follow [PEP 8](https://www.python.org/dev/peps/pep-0008/) conventions
- Use 4 spaces for indentation (not tabs)
- Keep line length under 100 characters
- Use descriptive variable and function names

### Code Organization
- Place imports at the top of the file in this order:
  1. Standard library imports
  2. Third-party imports
  3. Local imports
- Group related functionality in modules
- Keep functions focused and single-purpose

### Documentation
- Add docstrings to all public functions and classes
- Use Google-style docstrings format:
  ```python
  def example_function(param1: str, param2: int) -> bool:
      """Brief description of function.
      
      Longer description if needed, explaining the purpose,
      behavior, and any important details.
      
      Args:
          param1: Description of param1
          param2: Description of param2
      
      Returns:
          Description of return value
      
      Raises:
          ValueError: When something goes wrong
      """
  ```
- Comment complex logic and non-obvious decisions
- Keep comments up-to-date with code changes

### Testing
- Write unit tests using pytest
- Aim for at least 80% code coverage
- Test both success and error cases
- Use descriptive test names that explain what is being tested
- Place tests in a `tests/` directory mirroring the source structure

### Naming Conventions
- Functions and variables: `snake_case`
- Classes: `PascalCase`
- Constants: `UPPER_SNAKE_CASE`
- Private methods/attributes: prefix with `_`

## Pull Request Process

### Before You Start
1. Check the issues and pull requests to avoid duplicate work
2. Create an issue to discuss major features before implementing
3. Fork the repository and create a feature branch

### Creating a Pull Request
1. **Branch Naming**: Use descriptive names like:
   - `feature/user-authentication`
   - `bugfix/login-redirect-issue`
   - `docs/update-readme`

2. **Commit Messages**: Write clear, descriptive commit messages:
   - Use imperative mood: "Add feature" not "Added feature"
   - First line should be a short summary (50 characters max)
   - Provide additional context in the body if needed
   - Reference related issues: "Fixes #123"

3. **PR Description**: Include:
   - Brief description of changes
   - Motivation and context
   - Related issue numbers
   - Screenshots (if applicable)
   - Testing performed

4. **Code Review**:
   - Address feedback promptly
   - Respond to comments with explanations or changes
   - Push updates rather than force-pushing when possible
   - Be open to suggestions and improvements

5. **Checklist** (please verify before submitting):
   - [ ] Code follows the style guidelines
   - [ ] Self-review of code completed
   - [ ] Comments added for complex logic
   - [ ] Documentation updated if needed
   - [ ] No new warnings generated
   - [ ] Tests added/updated and passing
   - [ ] Code coverage not decreased
   - [ ] Commits have clear messages

### Merging
- PRs require at least one approval from a maintainer
- All CI/CD checks must pass
- Commits should be squashed if they represent a single logical change
- Maintainers will merge the PR once approved

## Development Setup

### Prerequisites
- Python 3.8 or higher
- pip or conda package manager
- Git

### Local Setup
```bash
# Clone your fork
git clone https://github.com/YOUR_USERNAME/fusionwrite-ai.git
cd fusionwrite-ai

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies in development mode
pip install -e ".[dev]"

# Install pre-commit hooks (optional but recommended)
pre-commit install
```

### Running Tests
```bash
# Run all tests
pytest

# Run with coverage
pytest --cov=fusionwrite_ai tests/

# Run specific test file
pytest tests/test_specific.py

# Run with verbose output
pytest -v
```

### Code Formatting and Linting
```bash
# Format code with Black
black .

# Check code style with Flake8
flake8 .

# Check type hints with mypy
mypy .
```

## Reporting Issues

When reporting a bug or requesting a feature, please:

1. **Check Existing Issues**: Ensure the issue hasn't been reported
2. **Provide Details**:
   - Clear, descriptive title
   - Step-by-step reproduction instructions
   - Expected vs. actual behavior
   - Error messages and stack traces
   - Environment information (OS, Python version, dependencies)
3. **Use Labels**: Apply appropriate labels (bug, feature, documentation, etc.)

### Example Bug Report
```
Title: Login fails with special characters in password

**Describe the bug:**
Users cannot log in if their password contains special characters like @ or !

**To Reproduce:**
1. Go to login page
2. Enter email: test@example.com
3. Enter password: myPass@123!
4. Click login
5. Error occurs

**Expected behavior:**
User should be authenticated successfully

**Environment:**
- OS: Ubuntu 20.04
- Python: 3.9.5
- Browser: Chrome 91.0
```

## Getting Help

- **Documentation**: Check the [README.md](README.md) and docs/ folder
- **Issues**: Search and create issues on GitHub
- **Discussions**: Use GitHub Discussions for questions
- **Email**: Contact maintainers (see MAINTAINERS.md)

## License

By contributing to FusionWrite AI, you agree that your contributions will be licensed under the project's license (see LICENSE file).

## Recognition

We appreciate all contributions! Contributors will be recognized in:
- The project README
- Release notes
- Contributor list

Thank you for making FusionWrite AI better! 🎉
