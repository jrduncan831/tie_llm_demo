# Installation Instructions using virtual environment (Windows)

This guide shows how to create a Python virtual environment on Windows and use it as a kernel in JupyterLab.

1. Check Python and pip

Open a Windows Command Prompt (or PowerShell) and run:

```bash
python --version
pip --version
```

If these commands are not recognized, install Python from python.org and make sure to check “Add Python to PATH” during installation.

2. Create a virtual environment

Navigate to your project folder and create a virtual environment (e.g., named .venv):

```bash 
cd \path\to\your\project
python -m venv .venv
```

This creates a folder .venv containing an isolated Python environment for your project.

3. Activate the virtual environment

In Command Prompt:

```bash 
.venv\Scripts\activate
```

In PowerShell (if you prefer):

```bash 
.venv\Scripts\Activate.ps1
```

You should see (.venv) at the beginning of your prompt, confirming the environment is active.

4. Install ipykernel and jupyterlab

Inside the activated environment, run:

```bash 
pip install -r requirements_3_11.txt
```

5. Register the environment as a Jupyter kernel

Still with the environment activated, run:

```bash 
python -m ipykernel install --user --name=project_name --display-name="My Project Environment"
```

Replace project_name with a short, unique name (no spaces), and adjust the display name as you like.
This adds a new kernel entry that JupyterLab will recognize.

You now should able to change the display-name kernel when opening jupyter lab IDE.  

Note: This is also possible with uv and conda and it maybe worth using if we need to specify python version. 
