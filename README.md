# python-hello-world

##You can use this repository to create a python egg file which can then be used to test for libration installation.

##Requirement:
* Python 2.7.x
* Setuptools - build tool to create python egg file
* easy_install - python library install tool

Note: This git repository already includes `hello-1.0-py2.7.egg` located under `dist` folder. 

You can simply download this file on your local machine and install it in you python environment using 
```python 
easy_install hello
```

###Using the HelloWorld module

```python
from hello import helloworld
print helloworld()
```

###Steps to create a python egg file:

* ```git clone https://github.com/ganeshchand/python-hello-world.git```
* ```cd python-helloworld```
* ```python setup.py bdist_egg```. This will create `hello-1.0-py2.7.egg` file under `dist` folder
* Below is the directory structure
```
python-hello-world/
| build
| dist/
    | hello-1.0-py2.7.egg
  hello/
  | __init__.py
    | hello.py
| hello.egg-info

```

where 
```build```, ```dist``` and ```hello.egg-info``` artifacts are generated as part of the build process.

```hello``` is a python package - a module that contains other modules; typically contained in a directory in the filesystem and distinguished from other directories by the presence of a file __init__.py.
```hello.py``` is a python module containg the source code.

```__init__.py``` is required to make Python treat the directory as a python package
