# Coding Conventions

[ [Back to README](README.md) ]

## General

The default variable and function name convention is camelCase.
This is the default for Go.

Please use descriptive variable names, and avoid single-character variables as general variables.
Single-character variables should only be used as index variables.

## Go (go-mms)

## Python (py-mms)

### Variable and Function Names

Python package function and variable names should mirror the corresponding names in the Go client.
Since the Go standard is to use camelCase, it is preferrable if the Python code does the same to avoid mixing conventions.

The convention in general for Python is to use snake case, however the standard allows for other formats for consistency, as in this case.

### Code Style

Generally, follow PEP8. However, PEP8 doesn't allow column alignment, which is otherwise the standard in Go.
Column alignment can sometimes make code easier to read, although it shouldn't be overused.

The GitHib workflow for `py-mms` uses the `flake8` tool to check code syntax on commits and pull requests.
Some of the checks are ignored, mostly those related to allowing for column alignment.

The following command can be used to check that the Python code follows the minimum set of syntax rules.
```bash
flake8 . --count --max-line-length=99 --ignore E203,E221,E226,E241,E251,E261,E266,E302,E305 --show-source --statistics
```
