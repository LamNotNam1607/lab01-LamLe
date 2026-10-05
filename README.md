# Study Assistant — Starter

A starter repository for the CSC10014 Smart Virtual Assistant project.

This project provides a simple study assistant that can answer basic questions
and serves as the starting point for further development.

---

## Requirements

Before setting up the project, make sure the following software is installed:

- Git
- Python 3
- pip
- Python virtual environment support (`venv`)

Check the installed versions with:

```bash
git --version
python3 --version
pip3 --version
```

If Python 3 is not installed on Ubuntu, install it with:

```bash
sudo apt update
sudo apt install python3 python3-pip python3-venv
```

---

## Setup

Follow these steps on a fresh machine.

### 1. Clone the repository

Clone the repository from GitHub:

```bash
git clone https://github.com/lhlam2507-collab/lab01-LamLe.git
```

Enter the project directory:

```bash
cd lab01-LamLe
```

### 2. Create a virtual environment

Create a Python virtual environment named `.venv`:

```bash
python3 -m venv .venv
```

The virtual environment keeps the project's Python packages separate from
the system Python installation.

### 3. Activate the virtual environment

On Ubuntu/Linux:

```bash
source .venv/bin/activate
```

After activation, the terminal prompt should contain:

```text
(.venv)
```

On Windows:

```powershell
.venv\Scripts\activate
```

### 4. Upgrade pip

After activating the virtual environment:

```bash
python -m pip install --upgrade pip
```

### 5. Install project dependencies

Install all required Python packages from `requirements.txt`:

```bash
pip install -r requirements.txt
```

Wait until the installation finishes successfully.

---

## Run

Before running the application, make sure the virtual environment is activated.

On Ubuntu/Linux:

```bash
source .venv/bin/activate
```

Run the starter assistant with:

```bash
python -m assistant "where is the IT helpdesk?"
```

The command sends the question:

```text
where is the IT helpdesk?
```

to the assistant.

If the command runs successfully, the application should return an answer
to the question.

---

## Test

The project uses `pytest` for automated testing.

Make sure the virtual environment is activated:

```bash
source .venv/bin/activate
```

Run the test suite with:

```bash
pytest -q
```

The `-q` option runs pytest in quiet mode so that the output is shorter and
easier to read.

All tests should pass before submitting the project.

---

## Environment Check

The project also contains a script for checking the development environment.

Run:

```bash
python scripts/check_env.py
```

If the script reports an error, check that:

1. Python 3 is installed.
2. The virtual environment is activated.
3. Project dependencies have been installed.
4. You are running the command from the project root directory.

---

## Project Structure

The project is organized into the following main components:

```text
lab01-LamLe/
├── assistant/
│   └── ...
├── scripts/
│   └── check_env.py
├── tests/
│   └── ...
├── requirements.txt
├── README.md
└── .gitignore
```

### `assistant/`

Contains the main source code of the study assistant.

This package contains the application logic used when running:

```bash
python -m assistant "where is the IT helpdesk?"
```

### `scripts/`

Contains utility scripts used to check or maintain the project.

For example:

```text
scripts/check_env.py
```

is used to check the development environment.

### `tests/`

Contains automated tests for the project.

The tests can be executed with:

```bash
pytest -q
```

### `requirements.txt`

Contains the Python dependencies required by the project.

Install them with:

```bash
pip install -r requirements.txt
```

### `README.md`

Contains the project documentation and setup instructions.

### `.gitignore`

Specifies files and directories that Git should not track.

In particular, the Python virtual environment must not be committed:

```text
.venv/
```

---

## Development Workflow

When working on the project, use the following workflow.

### 1. Activate the virtual environment

```bash
source .venv/bin/activate
```

### 2. Make your changes

Edit the source code, tests, or documentation as needed.

### 3. Run the environment check

```bash
python scripts/check_env.py
```

### 4. Run the tests

```bash
pytest -q
```

### 5. Check Git status

```bash
git status
```

Make sure that unnecessary files such as `.venv/` are not included in
the changes.

### 6. Commit your changes

Use a clear Conventional Commit message.

For example:

```bash
git add README.md
git commit -m "docs: update README"
```

---

## Git Ignore

The following files and directories should not be committed:

```text
.venv/
__pycache__/
*.pyc
.pytest_cache/
```

The `.venv/` directory contains the local Python virtual environment and can
be recreated using:

```bash
python3 -m venv .venv
```

Therefore, it should remain outside version control.

---

## Troubleshooting

### `python: command not found`

On Ubuntu/Linux, use `python3` to create the virtual environment:

```bash
python3 -m venv .venv
```

After activating the virtual environment:

```bash
source .venv/bin/activate
```

the `python` command should point to the Python interpreter inside `.venv`.

### `No module named venv`

Install Python's virtual environment package:

```bash
sudo apt update
sudo apt install python3-venv
```

Then create the environment again:

```bash
python3 -m venv .venv
```

### Dependencies are missing

Make sure the virtual environment is activated:

```bash
source .venv/bin/activate
```

Then install the dependencies:

```bash
pip install -r requirements.txt
```

### Tests fail

Run:

```bash
pytest -q
```

Read the error message carefully and check that:

- The virtual environment is activated.
- All dependencies are installed.
- You are in the project root directory.
- The required project files are present.

---

## Quick Start

For an experienced developer, the complete setup can be summarized as:

```bash
git clone https://github.com/lhlam2507-collab/lab01-LamLe.git
cd lab01-LamLe
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python -m assistant "where is the IT helpdesk?"
pytest -q
```

If all commands complete successfully, the project is ready for development.

---

## Submission Checklist

Before submitting the project, make sure that:

- [ ] The repository can be cloned successfully.
- [ ] The virtual environment can be created.
- [ ] The virtual environment can be activated.
- [ ] Dependencies can be installed from `requirements.txt`.
- [ ] The assistant can be run successfully.
- [ ] The test suite passes.
- [ ] `scripts/check_env.py` runs successfully.
- [ ] `.venv/` is included in `.gitignore`.
- [ ] There are no remaining `TODO` instructions in this README.
- [ ] The README contains clear setup, run, test, and project structure instructions.
