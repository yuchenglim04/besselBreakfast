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
