# arjuna-python documentation
Docs for Arjuna java Client
### Getting Started with Arjuna Frame work service

#### Prerequisities
Install the following artifacts
* Python 3.5+
* Github Desktop or Git Bash 
Clone the arjuna Source repo to a desired directory.

As a suggestion, don't clone inside a directory whose name is already arjuna.

`<arjuna_repo_root>` refers to the directory contains the arjuna repo. 

###### Command to clone arjuna repo
`git clone https://github.com/test-mile/arjuna.git`

######  Install third party libraries
using command `pip install <library_name>`
If pip in not recognized as a command, please set the path based on the operating system you are running or use `python3 -m pip install <library_name>` 
* requests
* pyhocon
* xlrd
* flask
* flask_restful
* waitress
* selenium

###### Launching setu.
Run the following command to launch setu

`<arjuna_repo_root>\arjuna\scripts>python3 arjuna_launcher.py launch-setu`
Prompts the following console out put

```
-------------------------------------------------
      ___         _
     / _ \       (_)
    / /_\ \ _ __  _  _   _  _ __    __ _
    |  _  || '__|| || | | || '_ \  / _` |
    | | | || |   | || |_| || | | || (_| |
    \_| |_/|_|   | | \__,_||_| |_| \__,_|
                _/ |
               |__/

-------------------------------------------------
Test Mile Arjuna
Version: 0.7.0-beta
Creator: Rahul Verma
(c) 2015-2019 Test Mile Software Testing Pvt Ltd
www.testmile.com
-------------------------------------------------
Parsing CLI Options...
Intializing Arjuna...
Executing Arjuna Command...
Launching Setu...
```


### Getting Started with Arjuna Python Client
