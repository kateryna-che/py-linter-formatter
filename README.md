# Linter Report Formatter

A small Python utility that converts raw Flake8-style linter output into a cleaner structure that is easier to display, store, or process later.

This repository is kept as a compact portfolio example: it shows working with dictionaries, lists, nested data structures, pure functions, and readable data transformation.

## What it does

The project contains three formatter functions:

- `format_linter_error` — converts one raw linter error into a normalized dictionary.
- `format_single_linter_file` — formats all errors for one file and adds a file status.
- `format_linter_report` — formats the full report for all checked files.

## Example

Input:

```python
error = {
    "code": "E501",
    "filename": "./source_code.py",
    "line_number": 18,
    "column_number": 80,
    "text": "line too long",
}
```

Output:

```python
{
    "line": 18,
    "column": 80,
    "message": "line too long",
    "name": "E501",
    "source": "flake8",
}
```

## Tech stack

- Python
- Pytest
- Flake8-style report format

## Local setup

```bash
git clone https://github.com/kateryna-che/py-linter-formatter.git
cd py-linter-formatter
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
pytest
```

## Status

Small portfolio exercise focused on data transformation and clean function design.
