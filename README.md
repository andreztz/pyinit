pyinit
=========
Make working with python virtualenv a breeze

If you switch to python from ruby and have worked with the ruby version manager (https://rvm.io) then virtualenv might feel as half baked.

Adding autoenv to automaticly enable virtualenvs is a huge step to make virtualenvs better.

Pyinit is a simple bash script to glue git, autoenv and virtualenv together.

1. It will install a .virtualenv folder into you're project folder and add it to .gitignore.
2. Initialize a new git project.
3. Install the project requirements mentioned in the requirement*.txt files. and configure autoenv so that the virtualenv will be activated if you enter the project directory.

To create a python3 based virtualenv:
```bash
[jb@vuurflits64 git]$ mkdir new-python3-project
[jb@vuurflits64 git]$ cd new-python3-project
[jb@vuurflits64 new-python3-project]$ pyinit python3

pyinit:
creating virtualenv
Already using interpreter /usr/bin/python3
Using base prefix '/usr'
New python executable in /home/jb/git/new-python3-project/.virtualenv/new-python3-project/bin/python3
Also creating executable in /home/jb/git/new-python3-project/.virtualenv/new-python3-project/bin/python
Installing setuptools, pip, wheel...done.
enable autoenv
initializing git project
Initialized empty Git repository in /home/jb/git/new-python3-project/.git/
[master (root-commit) c5a219f] initial commit
 1 file changed, 2 insertions(+)
 create mode 100644 .gitignore
use "cd ." to enable the new virtualenv

[jb@vuurflits64 new-python3-project]$ cd .
(new-python3-project) [jb@vuurflits64 new-python3-project]$
```
This script requires git, virtualenv autoenv, autoenv needs to be enabled in you're .bashrc or .zshrc file before using pyinit.

See https://pypi.python.org/pypi/autoenv/0.2.0 on how to install/enable autoenv
