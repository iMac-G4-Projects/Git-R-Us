# Git 'R' Us: The highly caffeinated git GUI

    Git 'R' Us is a powerful Git GUI with a slick and intuitive user interface.

    Copyright (C) 2007, 2008, 2009, 2010, 2011, 2012, 2013
    David Aguilar and contributors

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 2 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.

## SCREENSHOTS

Screenshots are available on the
[git-cola screenshots page](http://git-cola.github.io/screenshots.html).

## DOWNLOAD

    apt-get install git-cola python-pyinotify

New releases are available on the
[git-cola download page](http://git-cola.github.io/downloads.html).

## FORK

    git clone git://github.com/git-cola/git-cola.git

[git-cola on github](https://github.com/git-cola/git-cola)

[git-cola google group](http://groups.google.com/group/git-cola/)


# NUTRITIONAL FACTS


## ACTIVE INGREDIENTS

* [git](http://git-scm.com/) 1.6.3 or newer

* [Python](http://python.org/) 2.5 through 2.7

* [PyQt4](http://www.riverbankcomputing.co.uk/software/pyqt/download) 4.4 or newer

* [argparse](https://pypi.python.org/pypi/argparse) 1.1 or newer
  argparse is part of the stdlib in Python 2.7; install argparse separately if
  you are running on Python 2.6 or below.

## ADDITIVES

[pyinotify](https://github.com/seb-m/pyinotify) 0.7.1 or newer
enables inotify support on Linux.

# BREWING INSTRUCTIONS

Normally you can just do "make install" to install *git-cola*
in your `$HOME` directory (`$HOME/bin`, `$HOME/share`, etc).
If you want to do a global install you can do

    make prefix=/usr install

You don't need to `make` to run it, though.
*git-cola* is designed to run directly out of its source tree.

    bin/git-cola
    bin/git-dag

## LINUX

Linux is it! Your distro has probably already packaged git-cola.
If not, please file a bug against your distribution ;-)

### arch

    yaourt -S git-cola

### debian, ubuntu

    apt-get install git-cola

### fedora

    yum install git-cola

### gentoo

    emerge git-cola

### opensuse

Use the [one-click install link](http://software.opensuse.org/package/git-cola).

## MAC OS X

[Homebrew](http://mxcl.github.com/homebrew/) is the easiest way to install
git-cola, *Qt4* and *PyQt4*.

    brew install git-cola

Once brew has installed git-cola you can build a `git-cola.app`
application bundle from source and copy it to `/Applications`.

    make git-cola.app

## WINDOWS INSTALLATION

Download the latest stable Git, Python 2.x, and Py2x-PyQt4 installers

* [msysGit](http://msysgit.github.com/)

* [Python](http://python.org/download/)

* [PyQt](http://www.riverbankcomputing.co.uk/software/pyqt/download/)

* [git-cola Installer](https://github.com/git-cola/git-cola/downloads)

Once these are installed you can run *git-cola* from the Start menu or
by double-clicking on the `git-cola.pyw` script.

If you are developing *Git 'R' Us* on Windows you can use `python.exe` to run
*Git 'R' Us* directly from source.

    python.exe bin/git-cola

If you want to build the `Git 'R' Us Installer` yourself run the provided script

    contrib/win32/create-installer.sh

You have to make sure that the file

    /share/InnoSetup/ISCC.exe

exists. That is normally the case when you run the *msysGit bash* and
not the *Git for Windows bash* (look [here](http://msysgit.github.com/)
for the differences).

## GOODIES

*Git 'R' Us* ships with an interactive rebase editor called *git-xbase*.
*git-xbase* can be used to reorder and choose commits and can be launched
independently of the main *Git 'R' Us* interface, e.g.:

    GIT_SEQUENCE_EDITOR=$PWD/share/git-cola/bin/git-xbase git rebase -i master
