## Environment & Setup Notes (August 21, 2025)

### 1. Using Conda and Python in VS Code
- Added the following paths to my system’s PATH environment variable (only once):
	- For Python:
		- `C:\Users\gilld\AppData\Local\Programs\Python\Python312\`
		- `C:\Users\gilld\AppData\Local\Programs\Python\Python312\Scripts\`
	- For Conda:
		- `C:\Users\gilld\anaconda3`
		- `C:\Users\gilld\anaconda3\Scripts`
		- `C:\Users\gilld\anaconda3\Library\bin`

### 2. Initializing Conda for PowerShell
- To use `conda activate` in PowerShell (including VS Code’s terminal), run this command once in the Anaconda Prompt:
	```
	conda init powershell
	```
- Restart VS Code or your terminal after running this. You do not need to run it again unless you reset your PowerShell profile.

### 3. Managing Environments
- You do not need to add environment variables every time—just once during setup.
- You can use a single Conda environment (like `base`) for multiple projects to save disk space if they use similar libraries.
- Creating a `.venv` for every project uses more space, as each environment has its own copy of Python and all packages.
- Conda is more space-efficient because it shares packages between environments when possible.

### 4. Best Practices
- For reproducibility and to avoid package conflicts, create a new Conda environment for projects with different requirements.
- Clean up unused Conda environments with:
	```
	conda env remove -n <env_name>
	```
	and free up space with:
	```
	conda clean --all
	```

### 5. Troubleshooting
- If `conda` or `pip` is not recognized, check that the correct paths are in your PATH environment variable.
- Always restart VS Code or your terminal after changing environment variables or running `conda init`.

---
