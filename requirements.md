---
layout: lesson
root: .
---

## Requirements

 We will assume for this workshop that you are using a Linux PC: either a laptop or a remote machine that you can connect to using SSH. Ideally you will use your own laptop or connect to a system at your home institution: that way you will be able to continue using the same environment after the course. The software we will be using is available for Windows and Mac OSX too: you are welcome to run it on any OS you like, but we cannot offer much help during the sessions to get it working.

If you bring your own laptop and use it to connect to a remote machine, you will need to have an [SSH client][ssh] installed,
and will also need to set up and [export an X windows session][x-export] so that you can run graphical programs (ROOT and probably a text editor) on the remote machine.

[ssh]: http://en.wikipedia.org/wiki/Secure_Shell
[x-export]: http://www.linuxhowtos.org/Tips%20and%20Tricks/export_x.htm

The room we are using is equipped with Windows PCs running the Desktop@UCL environment, which has the necessary client software
installed. 

Whichever system you use for the actual exercises will need the following software installed:

* [Git][git] (version control system)
* [Python][python] 2.5+, but not version 3 (programming language and interpreter)
* [ROOT][root] (C++ data analysis toolkit) including the [PyROOT][pyroot] Python interface.
* [Nose][nose] Python testing toolkit
* a text editor of your choice

Ideally you should also have:

* [IPython][ipython]
* a [GitHub] account: you can sign up for free, and doing so in advance will save time during the course

[git]: http://git-scm.com/
[python]: http://www.python.org/
[root]: http://root.cern.ch/
[pyroot]: http://root.cern.ch/drupal/content/pyroot
[nose]: https://nose.readthedocs.org/en/latest/
[ipython]: http://ipython.org/
[GitHub]: https://github.com/

### Testing your environment

Check that you can run ROOT by typing

    root

and verifying that you see the ROOT splash screen and then a ROOT prompt

    root [0]

Check that you can start IPython and import the required modules:

    [waugh@goshawk ~]$ ipython 
    Python 2.7.3 (default, Aug  9 2012, 17:23:57) 
    Type "copyright", "credits" or "license" for more information.

    IPython 1.0.0 -- An enhanced Interactive Python.
    ?         -> Introduction and overview of IPython's features.
    %quickref -> Quick reference.
    help      -> Python's own help system.
    object?   -> Details about 'object', use 'object??' for extra details.

    In [1]: from ROOT import TFile

    In [2]: from nose import tools

or at least that you can do this using the default Python interpreter

    [waugh@goshawk ~]$ python
    Python 2.7.3 (default, Aug  9 2012, 17:23:57) 
    [GCC 4.7.1 20120720 (Red Hat 4.7.1-5)] on linux2
    Type "help", "copyright", "credits" or "license" for more information.
    >>> from ROOT import TFile
    >>> from nose import tools

If you get any errors when typing the `import` statements, then you do not have
the required modules installed, or your environment is not set up correctly to
find them.

### Examples

#### LXPlus

If you have an LXPlus account, all the required software is installed and accessible
by default.

#### UCL HEP cluster

Updated versions being installed...

#### Fedora Linux

On Fedora 18, and other recent versions, all the packages needed are available in the default repository
and can be installed using `yum install` or via the GUI by following Applications Menu -> Administration
-> Add/Remove Software. The packages you will need are

* `git`
* `python`
* `python-nose`
* `root` and other associated packages including `root-python`
* `python-ipython`

