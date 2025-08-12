<!-- Graphic-style Header -->
<p align="center">
  <img src="https://www.nmdp.org/-/media/project/nmdp/global/images/logos/nmdp_logo_tm_300x96.svg?h=33&iar=0&w=279&rev=3e13c88086fd4134b9c8588dd337bf15&hash=962753EC04F56EC53A91717E3F2DB963" alt="NMDP" width="150"/>
</p>
<!-- Graphic-style Header -->
<p align="center">
  <img src="https://immunepolymorphismsociety.org/img/logo120.png" alt="Society for Immune Polymorphism" width="120" />
</p>

# Contributing to the FHIR Profile for HLA Antibody Reporting

Thank you for your interest in contributing to the FHIR profile for HLA Antibody Reporting! We welcome contributions from everyone.

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check the existing issues to avoid duplicates. When you create a bug report, include as many details as possible:

- **Use a clear and descriptive title**
- **Describe the exact steps to reproduce the problem**
- **Provide specific examples to demonstrate the steps**
- **Describe the behavior you observed and what behavior you expected**
- **Include screenshots if applicable**
- **Include your environment details** (OS, browser version, etc.)

Use the bug report template when available.

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion:

- **Use a clear and descriptive title**
- **Provide a detailed description of the suggested enhancement**
- **Explain why this enhancement would be useful**
- **List some other projects where this enhancement exists, if applicable**

### Pull Requests

1. **Fork the repository** and create your branch from `main`
2. **Install dependencies**: `npm install` (or your package manager)
3. **Make your changes** in a feature branch
4. **Add tests** for any new functionality
5. **Ensure the test suite passes**: `npm test`
6. **Run the linter**: `npm run lint`
7. **Update documentation** if needed
8. **Commit your changes** using conventional commit format
9. **Push to your fork** and submit a pull request

#### Pull Request Guidelines

- Fill in the provided template
- Include the relevant issue number if applicable
- Update the README.md with details of changes if needed
- Increase version numbers following [SemVer](http://semver.org/)
- Ensure your code follows the existing style conventions

## Development Setup

### Prerequisites

- npm or yarn
- sushi

### Local Development

```bash
# Clone your fork
git clone https://github.com/yourusername/project-name.git

# Navigate to the project directory
cd project-name

# Install dependencies
npm install

# Start development server
npm run dev

# Run tests
npm test

# Run linting
npm run lint
```

## Style Guidelines

### Git Commit Messages

- Use the present tense ("Add feature" not "Added feature")
- Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit the first line to 72 characters or less
- Reference issues and pull requests liberally after the first line
- Follow [Conventional Commits](https://www.conventionalcommits.org/) format:
    - `feat:` for new features
    - `fix:` for bug fixes
    - `docs:` for documentation changes
    - `style:` for formatting changes
    - `refactor:` for code refactoring
    - `test:` for adding tests
    - `chore:` for maintenance tasks

### Code Style

- Follow the existing code style in the project
- Use meaningful variable and function names
- Add comments for complex logic
- Keep functions small and focused
- [Add any specific style guidelines for your language/framework]

### Documentation

- Update README.md if your changes affect usage
- Add JSDoc comments for new functions/classes
- Update API documentation if applicable
- Include examples in documentation when helpful

## Testing

- Write tests for new features and bug fixes
- Ensure all tests pass before submitting PR
- Aim for good test coverage
- Include both unit tests and integration tests where appropriate

## Questions?

If you have questions about contributing, please:

- Check existing issues and discussions
- Create a new issue with the "question" label
- Reach out in our fhir@nmdp.org

## Recognition

Contributors will be recognized in our [CONTRIBUTORS.md](CONTRIBUTORS.md) file and release notes.

## License

By contributing to the FHIR profile for HLA Antibody Reporting, you agree that your contributions will be licensed under the same license as the project (see LICENSE).

---

Thank you for contributing! 🎉