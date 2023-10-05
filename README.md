python -m venv "the name of the environment" for example "stat-env"

Do this command inside your project at the root.

To activate do: \Environment\Scripts\Activate and you will see that you are inside that environment

![image](https://github.com/OlofssonFredrik/Virtual-Env/assets/107762409/d4700160-f16c-4508-91d2-8e4b4aa6fc56)

This will however raise a flag that powershell is not allowed to perform such scripts. 

In order to allow temporary you can run: Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process

If you want to permanety allow run: Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser

