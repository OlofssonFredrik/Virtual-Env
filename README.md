python -m venv "the name of the environment" for example "stat-env"

Do this command inside your project at the root.

To activate do: .\Environment\Scripts\Activate and you will see that you are inside that environment

![image](https://github.com/OlofssonFredrik/Virtual-Env/assets/107762409/d4700160-f16c-4508-91d2-8e4b4aa6fc56)

This will however raise a flag that powershell is not allowed to perform such scripts. 

In order to allow temporary in this powershell window you can run: Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process

If you want to permanety allow run: Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser

Setting Up and Using Virtual Environments with Python and GitHub When working with Python projects, it's often recommended to create a virtual environment to manage dependencies and ensure consistency across different systems. Follow the steps below to create and manage a virtual environment for your project.

Creating a Virtual Environment In your terminal or command prompt, navigate to your project's root directory and run the following command:
sh Copy code python -m venv [environment_name] Replace [environment_name] with your desired environment name, for instance, "stat-env".

Example:

sh Copy code python -m venv stat-env 2. Activating the Virtual Environment Navigate to your project root, and activate the virtual environment with:

Windows (PowerShell):

PowerShell Copy code .\stat-env\Scripts\Activate Note: If you encounter a PowerShell security error about scripts, follow the instructions in the PowerShell Script Execution Policies section below.

Linux/MacOS:

sh Copy code source stat-env/bin/activate Upon activation, your command prompt should change to indicate that the virtual environment is active:

sh Copy code (stat-env) [your_directory_path]$ PowerShell Script Execution Policies PowerShell restricts the execution of scripts for security reasons. To bypass these restrictions for activating a virtual environment, you have a couple of options:

Option A: Temporarily Bypass the Execution Policy Allow the script to run in the current PowerShell session only:

PowerShell Copy code Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process Then, run the activate script again.

Option B: Change the Execution Policy for the Current User Allow local scripts to run for your user profile while maintaining the restriction against running remote scripts:

PowerShell Copy code Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser You will only need to do this once per user. Remember, it's a good practice to understand the risks of modifying execution policies. Always ensure scripts are from a trusted source before executing them.

Deactivating the Virtual Environment To exit the virtual environment and use your global Python configuration again, simply type:
sh Copy code deactivate Final Notes Always remember to activate the virtual environment before running your project and deactivate it when you're done. Virtual environments help you manage project dependencies and keep your global Python environment clean and organized.

For additional details and best practices about virtual environments, visit the Python venv documentation.
