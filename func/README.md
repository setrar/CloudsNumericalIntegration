

```
func init --python                           
```
> Returns
```powershell
Found Python version 3.12.7 (python3).
The new Python programming model is generally available. Learn more at https://aka.ms/pythonprogrammingmodel
Writing requirements.txt
Writing function_app.py
Writing .gitignore
Writing host.json
Writing local.settings.json
Writing /Users/valiha/Developer/CloudsNumericalIntegration/func/.vscode/extensions.json
```


```
func new --template "HTTP trigger" --name MyPythonFunction
```
> Returns
```powershell
Select a number for Auth Level:
1. FUNCTION
2. ANONYMOUS
3. ADMIN
Choose option: 2
Appending to /Users/valiha/Developer/CloudsNumericalIntegration/func/function_app.py
The function "MyPythonFunction" was created successfully from the "HTTP trigger" template.
```

```
func azure functionapp publish clouds25lab2eurbrniapp
```
> Returns
```powershell
func azure functionapp publish clouds25lab2eurbrniapp
Local python version '3.12.7' is different from the version expected for your deployed Function App. This may result in 'ModuleNotFound' errors in Azure Functions. Please create a Python Function App for version 3.12 or change the virtual environment on your local machine to match ''.
Getting site publishing info...
[2025-01-25T05:45:18.747Z] Starting the function app deployment...
Updating Application Settings for Remote build...
Creating archive for current directory...
Performing remote build for functions project.
Uploading 3.46 KB [###############################################################################]
Remote build in progress, please wait...
Updating submodules.
Preparing deployment for commit id '31fd1ff7-0'.
PreDeployment: context.CleanOutputPath False
PreDeployment: context.OutputPath /home/site/wwwroot
Repository path is /tmp/zipdeploy/extracted
Running oryx build...
Command: oryx build /tmp/zipdeploy/extracted -o /tmp/build/expressbuild --platform python --platform-version 3.6.15 -i /tmp/8dd3d0428614de3 -p packagedir=.python_packages/lib/site-packages
Operation performed by Microsoft Oryx, https://github.com/Microsoft/Oryx
You can report issues at https://github.com/Microsoft/Oryx/issues

Oryx Version: 0.2.20250107.1+ef3fb2f9c490a4fbb1f76b5746cd4ba2ff0409f4, Commit: ef3fb2f9c490a4fbb1f76b5746cd4ba2ff0409f4, ReleaseTagName: 20250107.1

Build Operation ID: 947a7412197a9b2e
Repository Commit : 31fd1ff7-09ad-4d06-9a84-f7df166c7092
OS Type           : buster
Image Type        : githubactions

Detecting platforms...
Detected following platforms:
  python: 3.6.15
Version '3.6.15' of platform 'python' is not installed. Generating script to install it...
Warning: An outdated version of python was detected (3.6.15). Consider updating.\nVersions supported by Oryx: https://github.com/microsoft/Oryx


Using intermediate directory '/tmp/8dd3d0428614de3'.

Copying files to the intermediate directory...
Done in 0 sec(s).

Source directory     : /tmp/8dd3d0428614de3
Destination directory: /tmp/build/expressbuild


Downloading and extracting 'python' version '3.6.15' to '/tmp/oryx/platforms/python/3.6.15'...
Detected image debian flavor: buster.
Downloaded in 6 sec(s).
Verifying checksum...
Extracting contents...
performing sha512 checksum for: python...
Done in 19 sec(s).

Python Version: /tmp/oryx/platforms/python/3.6.15/bin/python3.6
Creating directory for command manifest file if it does not exist
Removing existing manifest file

Running pip install...
Done in 8 sec(s).
[05:50:59+0000] Processing /home/conda/feedstock_root/build_artifacts/archspec_1708969572489/work
ERROR: Could not install packages due to an OSError: [Errno 2] No such file or directory: '/home/conda/feedstock_root/build_artifacts/archspec_1708969572489/work'

WARNING: You are using pip version 21.2.4; however, version 21.3.1 is available.
You should consider upgrading via the '/tmp/oryx/platforms/python/3.6.15/bin/python3.6 -m pip install --upgrade pip' command.
"2025-01-25 05:51:01"|ERROR|[05:50:59+0000] Processing /home/conda/feedstock_root/build_artifacts/archspec_1708969572489/work
ERROR: Could not install packages due to an OSError: [Errno 2] No such file or directory: '/home/conda/feedstock_root/build_artifacts/archspec_1708969572489/work'

WARNING: You are using pip version 21.2.4; however, version 21.3.1 is available.
You should consider upgrading via the '/tmp/oryx/platforms/python/3.6.15/bin/python3.6 -m pip install --upgrade pip' command. | Exit code: 1 | Please review your requirements.txt | More information: https://aka.ms/troubleshoot-python
\n/opt/Kudu/Scripts/starter.sh oryx build /tmp/zipdeploy/extracted -o /tmp/build/expressbuild --platform python --platform-version 3.6.15 -i /tmp/8dd3d0428614de3 -p packagedir=.python_packages/lib/site-packages

Generating summary of Oryx build
Deployment Log file does not exist in /tmp/oryx-build.log
The logfile at /tmp/oryx-build.log is empty. Unable to fetch the summary of build
Deployment Failed. deployer = Push-Deployer deploymentPath = Functions App ZipDeploy. Extract zip. Remote build.
Remote build failed!
```




