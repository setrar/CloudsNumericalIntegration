

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

The Auth Level specifies the level of access control for your Azure Function. Here’s what each option means:
	1.	FUNCTION: Requires a function key to access the function. The key must be included in the request URL.
	•	Use this for controlled access at the function level.
	•	Example:

https://<function-app-name>.azurewebsites.net/api/MyPythonFunction?code=<function-key>


	2.	ANONYMOUS: No authentication required. Anyone with the URL can access the function.
	•	Use this for publicly accessible functions.
	•	Example:

https://<function-app-name>.azurewebsites.net/api/MyPythonFunction


	3.	ADMIN: Requires an admin key to access the function. This is more restrictive than the FUNCTION level.
	•	Typically used for internal management or debugging purposes.

Recommendation

For most use cases, choose option 2 (ANONYMOUS) to simplify testing and public access:

Choose option: 2

You can later configure the authentication level for production deployments via the Azure Portal or the function.json file.
```




