# Python lesson 001 #

*By Teddy Morduhovich, 2018*

---

```python
print('hello world!')
```

in this tutorial, we will set up everything we need to program python scripts on windows.


I found out through a lot of trial and error that you need some pre-requisites you need before starting to avoid quite a few errors and bugs.

this is a platform specific tutorial, so this will focus on setting things up for Windows (this tutorial uses windows 10)

in order to get everything (or at least most of the things) ready for python development!

we will be using the latest stable release of python, python 3.6.5

you can download it here [Python 3.6.5 for Windows](https://www.python.org/ftp/python/3.6.5/python-3.6.5.exe).

install python and include it in your PATH directory, you can simply check that tickbox during installation to avoid using cmd commands later on.


now we need a few additional stuff to make sure we don't run into errors during `pip3` commands later on since it needs a few dependencies
to compile the modules it fetches.

I found that this 2 things made most modules compile successfully:

* Visual C++ Build tools 14
* Visual C++ Build tools 17

Visual C++ Build tools 14 is included in every release of Visual Studio 2015, so if you have that installed you have that already!
Visual C++ Build tools 17 is included in every release of Visual Studio 2017, so if you have that installed you have that already!

I simply installed both versions of Visual Studio 2015+2017 Community Editions.

but if you don't want to install additional IDEs you can simply find them in your Microsoft developer account in the downloads section
and install the build tools only.

now more or less you have everything set up to be able to start creating basic python scripts!

to simplify and isolate things we will be using virtual environments to develop in python using `venv` and we will create a new virtual
environment for every new project.

to create a new virtual environment simply use the following command via cmd:

`python -m venv <PATH>`

example for a path: `C://pythonenv/venv01/`

example command `python -m venv C://pythonenv/venv01/`

this will create a new virtual environment in the directory `C://pythonenv/venv01`

to activate the environment simply use the following command:

`<PATH>/Scripts/activate.bat`

in our case it will look like this:

`C://pythonenv/venv01/Scripts/activate.bat`

the cmd should look like this: 

`(venv01) C:\python_env\venv01>`

congrats! you are now inside the virtual environment!

now we can either launch a python interpreter (simply type in `python` to start one) or install modules via `pip3` commands!

to install a module simply use the following command:

`pip3 install <MODULE>` where `<MODULE>` is the modules name.

example uses:

* `pip3 install tensorflow`
* `pip3 install flask`
* `pip3 install matplotlib`

and so on!

if you have any questions, just submit a comment!
good luck!
