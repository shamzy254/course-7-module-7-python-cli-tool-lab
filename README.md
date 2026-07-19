# Python CLI Task Manager

## Overview

This project implements a small command-line task manager using Python's built-in `argparse` module and object-oriented programming. It allows users to create a task for a named user and mark that task as complete while providing helpful feedback in the terminal.

## Features

- Add tasks with the `add-task` command
- Complete tasks with the `complete-task` command
- Organize tasks under user objects using the `User` class
- Keep task state in the `Task` class with a completion flag
- Provide clear terminal messages for success and error cases

## Project Structure

- `lib/models.py` defines the `Task` and `User` classes
- `lib/cli_tool.py` defines the CLI commands and command routing
- `testing/test_cli_tool.py` contains basic end-to-end tests for the CLI

## Setup

Create and activate a virtual environment if desired:

```bash
python -m venv venv
source venv/bin/activate  # macOS/Linux
venv\Scripts\activate   # Windows
```

Install the test dependency:

```bash
python -m pip install pytest
```

## Usage

Add a task:

```bash
python -m lib.cli_tool add-task Alice "Write unit tests"
```

Complete a task:

```bash
python -m lib.cli_tool complete-task Alice "Write unit tests"
```

## Testing

Run the test suite:

```bash
python -m pytest -q
```

## Example Output

```text
📌 Task 'Write unit tests' added to Alice.
✅ Task 'Write unit tests' completed.
```
