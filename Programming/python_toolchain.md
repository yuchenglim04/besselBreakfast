# pip
```
pip --version

python -m pip install --upgrade pip

pip install <package_name>

py -m pip insitall pip==21.1.1

pip show <package_name>

pip list

pip list -v                               # list with file location

pip install <package_name> --upgrade

pip uninstall <package_name>
```

# Virtual Environment
```
https://smuhabdullah.medium.com/how-to-use-different-python-versions-with-virtualenv-907b2998b16e
install python 3.11 from https://www.python.org/downloads/release/python-3119/
pip install virtualenv
mkdir C:\pythonEnv
cd  C:\pythonEnv
virtualenv -p python3.12 myenv3.12
virtualenv -p python3.11 myenv3.11
myenv3.11\Scripts\activate


```


```
pip install virtualenv   
mkdir <folder_name>  
cd <folder_name>  
python<version> -m venv <virtual-environment-name>  
```


e.g.  
```python3.8 -m venv env```

Activate:  
```source env/bin/activate```

Check that it is a virtual evironment  
```pip list```

 ```~ deactivate```

How do I remove/delete a virtualenv?  
https://stackoverflow.com/questions/11005457/how-do-i-remove-delete-a-virtualenv
