## Install UV

## On Powershell
- irm https://astral.sh/uv/install.ps1 | iex  or pip install uv
- verify version uv --version

## UV Commands
- uv init : Initialize project, gitignore, main.py and pyproject.toml, pyhton-version files
- uv sync : creates .env and install dependencies
- uv add  : to add dependencies

## Select Kernel on VSCode

### Activate Environment

- Open VS Code terminal and activate your env.
- .venv\Scripts\activate
- pip install ipykernel (Not required if installed jupyter extensions)
- Open any ipynb file
- Select Kernal and Select your environment
