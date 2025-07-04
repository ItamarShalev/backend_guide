# Getting Started

This guide explains how to set up and run the FastAPI backend using [uv](https://github.com/astral-sh/uv), a fast Python package manager.

## Prerequisites

- Docker installed, see [Install Docker](https://docs.docker.com/get-docker/)
- Python 3.13 or newer installed [Python official page](https://www.python.org/downloads/)
- [uv](https://github.com/astral-sh/uv) installed, see [Install 'uv'](#1-install-uv)

## Environment variables
To make sure the terminal can find your python and uv executables, you need to add the paths to your environment variables.

Assuming your python.exe file located at: `C:\Users\<username>\AppData\Local\Programs\Python\Python3.13\python.exe`

You should add the following to your 'PATH' environment variable:
```bash
C:\Users\<username>\AppData\Local\Programs\Python\Python3.13
``` 

For more help you can see the following video: [How to add Python to PATH on Windows](https://www.youtube.com/watch?v=91SGaK7_eeY)


## 1. Install `uv`

#### Using pip

```bash
python -m pip install uv
```

#### Using the installer

[uv official page](https://docs.astral.sh/uv/getting-started/installation/).

## 2. Install Project Dependencies

#### Development Mode
```bash
uv sync --dev
```

## 3. Run the FastAPI Application

```bash
uv run fastapi dev main.py
```

## 4. Access the API

Open your browser and go to: [http://127.0.0.1:8000](http://127.0.0.1:8000)

### Swagger UI

The interactive API docs are available at: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

### Redoc

The alternative API docs are available at: [http://127.0.0.1:8000/redoc](http://127.0.0.1:8000/redoc)


## 5. Add new dependencies

#### For development dependencies

```bash
uv add <package_name> --dev
```

#### For production dependencies

```bash
uv add <package_name>
```

## 6. Check the code before committing
```bash
uv run pre-commit run
```

## 7. Make it automatic
To automatically run checks before committing, you can set up pre-commit hooks. This is already configured in the `.pre-commit-config.yaml` file.
To install the pre-commit hooks, run:
```bash
uv run pre-commit install
```
