- 16-01-25 23:02
- Sources: [[Python environments in VS Code - Visual Studio Code]]
- Links: [[Python]], [[Virtual Environment]]
---
# Setting up a Virtual Environment (venv) in VS Code on Ubuntu

## 1. Create a Virtual Environment
1. **Navigate to your project folder**.
2. **Create a virtual environment** using the following command:
```bash
python3 -m venv .venv
```
   - `.venv` is the standard folder name for virtual environments.
   - This command creates a `.venv` folder containing the virtual environment's Python interpreter and installed packages.
---
## 2. Activate the Virtual Environment
Activate the virtual environment to use it for your project:
```bash
source .venv/bin/activate
```
- After activation, your terminal prompt should change to reflect the virtual environment, e.g., `(.venv)`.
---
## 3. Open the Project in VS Code
1. Open VS Code:
```bash
code .
```
- The `code .` command opens the current directory in VS Code.
2. **Install project-specific dependencies** (if any):
```bash
pip install -r requirements.txt
```
- *(Skip this if there's no `requirements.txt` file yet.)*
---
## 4. Configure VS Code to Use the Virtual Environment
1. **Select the Python Interpreter**:
   - Press `Ctrl+Shift+P` to open the Command Palette.
   - Search for `Python: Select Interpreter`.
   - From the list, choose the interpreter inside `.venv`. It will look like:
```
~/Projects/MyProject/.venv/bin/python
```
2. **Verify the Interpreter**:
   - Open the terminal inside VS Code (`Ctrl+` or `View > Terminal`).
   - Run:
```bash
python --version
```
   - It should display the version of Python in your virtual environment.
---
## 5. Test the Setup
1. Create a sample Python file (`test.py`) in your project directory:
```python
print("Hello, Virtual Environment!")
```
2. Run the script using the terminal or VS Code's built-in Run option:
```bash
python test.py
```
---
## 6. Add `.gitignore` for Version Control
To avoid committing your virtual environment to Git, add a `.gitignore` file in the project directory with the following content:
```
.venv/
```
---
## 7. Deactivate the Virtual Environment
When you're done working, deactivate the virtual environment:
```bash
deactivate
```
---
## 8. Reactivate the Virtual Environment
Whenever you return to the project, re-enter the environment:
```bash
cd ~/Projects/MyProject
source .venv/bin/activate
```