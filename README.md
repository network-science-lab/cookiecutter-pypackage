# Cookiecutter - simple pypackage

Simple template for a Python package.

## Requirements

``` bash
pip install -U cookiecutter
```

## Usage 

```bash
cookiecutter https://github.com/network-science-lab/cookiecutter-pypackage.git
```
`authors` should be separeted by `,`.

## Developer Tips

### General

Try to keep your code simple. \
Remember to declaring types and try to avoid type `Any`. \
Use apropriete commit names to make it easier for other people understanding your code (Convetional Commits specification - https://www.conventionalcommits.org/en/v1.0.0/)

### Tests

It is important part of developing features to providing test cases that will allow to check different use cases (happy path, expected errors etc). We strongly suggest committing to `pytest` as our testing tool. All tests should be organized in `tests` module, python files should have `test` prepend in the name as well as testing functions. Good test should have 3 seperated parts:
1. Arrange - preparing input for tested functionality,
2. Act - invoking functionality,
3. Assert - checking whether the test case ended as expected.

### Formating

Remember to use code formatting tools and verify is everything alright before pushing changes by using `tox`.

``` bash
pip install -U black isort flake8 mypy pylint tox
```

Usage

``` bash
black <DIR>
isort <DIR>
flake8 <DIR>
mypy <DIR>
pylint <DIR>
tox
```

### Code Review

Never push commits to master branch, create seperate for functionalities that you are developing and create appropriete pull requests

1. Remember to assign yourself to your PR,
2. Request to at least 2 other people to review your changes,
3. Put the PR updates in the separate commits for making easier reviewing the changes,
4. Before the merge squash commits for clarity in the git history.