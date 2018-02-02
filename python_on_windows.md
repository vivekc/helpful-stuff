## Tip to setting up Python 3 virtual environment on windows 

If you are behind a proxy, run the following commands on windows command prompt to setup proxy settings:
```bash
set http_proxy=http://username:password@proxy_host:proxy_port
set https_proxy=https://username:password@proxy_host:proxy_port
```
If your username or password contains an `@` you can percent-encode (URL encode) it as `%40`.
#
#### 0. Hit following commands to set the environment variables:
```bash
D:\vivekc>set PYTHON_PATH=D:\python
D:\vivekc>set PYTHON_SCRIPT_PATH=D:\python\Scripts
```
#
#### 1. Create A Virtual Environment
```bash
D:\vivekc>%PYTHON_SCRIPT_PATH%\pip.exe install virtualenv
D:\vivekc>%PYTHON_SCRIPT_PATH%\virtualenv.exe myvirtualenv
```
#
#### 2. Activate Virtual Environment
```bash
D:\vivekc>D:\vivekc\myvirtualenv\Scripts\activate
```
This command will set an environment variable `VIRTUAL_ENV` with value as "**myvirtualenv**" and display a prefix "**(myvirtualenv)**" to the command prompt.

To check the path to your newly activated virtual environment
```
(myvirtualenv) D:\vivekc>echo %VIRTUAL_ENV%
```
#
##### 3. Until the virtual environment is deactivated, commands `python` and `pip` will refer to the location of virtual environment. This can be verified with below commands:
```
(myvirtualenv) D:\vivekc> where python
```
will display
`output:D:\vivekc\myvirtualenv\Scripts\python.exe`

and
```
(myvirtualenv) D:\vivekc> where pip
```
will display
`D:\vivekc\myvirtualenv\Scripts\pip.exe`

Until the Virtual Environment is active, all subsequent `pip install <package>` commands will install all packages relative to the virtual environment path
i.e. `%VIRTUAL_ENV%\Lib\site-packages`

#
##### 4. Deactivate Virtual Environment
```
(myvirtualenv) D:\vivekc>deactivate
```
