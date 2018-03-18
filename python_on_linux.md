# Tip to setting up Python 3 virtual environment on Linux OS

```bash
$ virtualenv -p `which python3` python3env
```

It is possible that you have multiple versions of python installed on your local machine.
In general, command ```python``` refers to python>=2.7 executable, whereas ```python3``` command refers to python>=3.0 executable.

When creating a new virtualenv, you might need to specify which version of python should be used. 
```which <command>``` command shows you which directory contains the executable for a particular ```<command>```.

```virtualenv``` command supports a ```-p``` flag to specify path to a particular python executable. PFB Documentation

```
 -p PYTHON_EXE, --python=PYTHON_EXE
                        The Python interpreter to use, e.g.,
                        --python=python2.5 will use the python2.5 interpreter
                        to create the new environment.  The default is the
                        interpreter that virtualenv was installed with
                        (/usr/bin/python)
```

Combine this with the ```which python3``` command, and you get your python3 virtualenv up and running.
