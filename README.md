# Setting Up Virtual Environments with Python and Windows
When working with Python projects, it's often recommended to create a virtual environment to manage dependencies and ensure consistency across different systems. Follow the steps below to create and manage a virtual environment for your project.

## Creating a Virtual Environment In your terminal or command prompt, navigate to your project's root directory and run the following command:
python -m venv [environment_name] 

Replace [environment_name] with your desired environment name, for instance, "stat-env".

## Example:
py -3.9 -m venv testar-env

python -m venv stat-env

Do this command inside your project at the root.

To activate do: .\stat-env\Scripts\Activate and you will see that you are inside that environment

![image](https://github.com/OlofssonFredrik/Virtual-Env/assets/107762409/d4700160-f16c-4508-91d2-8e4b4aa6fc56)

## Note: If you encounter a PowerShell security error about scripts, follow the instructions in the PowerShell Script Execution Policies section below.

### Option A: Temporarily Bypass the Execution Policy Allow the script to run in the current PowerShell session only:

Copy and Paste into powershell: Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process

Then, run the activate script again.

### Option B: Change the Execution Policy for the Current User Allow local scripts to run for your user profile while maintaining the restriction against running remote scripts:

Copy and Paste into powershell: Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser

You will only need to do this once per user. Remember, it's a good practice to understand the risks of modifying execution policies. Always ensure scripts are from a trusted source before executing them.

### Deactivating the Virtual Environment 
To exit the virtual environment and use your global Python configuration again, simply type: deactivate

Always remember to activate the virtual environment before running your project and deactivate it when you're done. Virtual environments help you manage project dependencies and keep your global Python environment clean and organized.

For additional details and best practices about virtual environments, visit the Python venv documentation.
