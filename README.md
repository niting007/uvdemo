UV FastAPI Demo Project – Setup & Run Guide
1. Create a project folder

Choose or create a directory where you want to store the project files.
2. Ensure Python is installed

Verify that Python 3.8 or higher is installed on your system. You can check by running:

```bash
python --version
```
3. Install UV

Install UV globally on your machine:
```bash
pip install uv
```
4. Install project dependencies

Run the following command inside your project folder:
```bash
uv run
```
This will:

    Create a .venv virtual environment folder.

    Install all dependencies listed in the pyproject.toml file.

5. Install FastAPI and Uvicorn (if not already included)

If FastAPI and Uvicorn are not in the pyproject.toml, install them manually:

```bash
uv pip install fastapi uvicorn
```

6. Create the FastAPI application

Example main.py:

```bash
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"message": "Hello, FastAPI with UV!"}
```
7. Run the FastAPI server

Start the development server with:
```bash
uv run uvicorn main:app --reload

    main:app → Refers to the app instance inside main.py.

    --reload → Enables auto-restart when code changes.
```
8. Test the application

Open your browser and visit:
```bash
    API root: http://127.0.0.1:8000

    API docs (Swagger UI): http://127.0.0.1:8000/docs
```

9. If you want to add runtime any library then we need to run below command
```bash
    uv add fastapi 

    uv add uvicorn

```