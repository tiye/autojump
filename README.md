% autojump(1) release-v19
% 
% 07 April 2012

NAME
----

autojump - a faster way to navigate your filesystem

SYNOPSIS
--------

Jump to a previously visited directory 'foobar':

    j foo

Show all database entries and their respective key weights:

    jumpstat

DESCRIPTION
-----------

autojump is a faster way to navigate your filesystem. It works by
maintaining a database of the directories you use the most from the
command line. The jumpstat command shows you the current contents of the
database. Directories must be visited first before they can be jumped
to.

autojump supports tab completion in Bash v4.0+.

OPTIONS
-------

Below options must be passed to 'autojump' and not the 'j' wrapper
function.

    -a, --add DIR       manually add path to database

    --stat              show database entries and their key weights

    --version           show version information and exit

INTERNAL OPTIONS
----------------

    -b, --bash

    --completion        prevent key weight decay over time

ADVANCED USAGE
--------------

To manually change an entry's weight, edit the file
$XDG\_DATA\_HOME/autojump/autojump.txt.

FILES
-----

If installed locally, autojump is self-contained in the directory
\~/.autojump/.

The database is stored in $XDG\_DATA\_HOME/autojump/autojump.txt.

REPORTING BUGS
--------------

For any issues please visit the following URL:

https://github.com/joelthelion/autojump/issues

THANKS
------

Special thanks goes out to: Pierre Gueth, Simon Marache-Francisco,
Daniel Jackoway, and many others.

AUTHORS
-------

autojump was originally written by Joël Schaerer, and currently
maintained by William Ting.

COPYRIGHT
---------

Copyright © 2012 Free Software Foundation, Inc. License GPLv3+: GNU GPL
version 3 or later <http://gnu.org/licenses/gpl.html>. This is free
software: you are free to change and redistribute it. There is NO
WARRANTY, to the extent permitted by law.

INSTALLATION
------------

### REQUIREMENTS

Python v2.6+ or 3.0+

### AUTOMATIC INSTALLATION

**Linux**

autojump is included in the following distro repositories, please use
relevant package management utilities to install (e.g. yum, apt-get,
etc):

    - Debian testing/unstable, Ubuntu, Linux Mint

    On Debian only, autojump requires manual activation for policy reasons. Please see ``/usr/share/doc/autojump/README.Debian``.

    - RedHat, Fedora, CentOS
    - ArchLinux
    - Gentoo
    - Frugalware
    - Slackware

**Mac**

Homebrew is the recommended installation method for Mac OS X::

    brew install autojump

A MacPorts installation method is also
[available](https://trac.macports.org/browser/trunk/dports/sysutils/autojump/Portfile).

**Other**

Please check the [Wiki](https://github.com/joelthelion/autojump/wiki)
for an up to date listing of installation methods.

### MANUAL INSTALLATION

Grab a copy of autojump::

    git clone git://github.com/joelthelion/autojump.git

Run the installation script::

    cd autojump
    ./install.sh [ --local ] [ --zsh ]

and follow on screen instructions.

### MANUAL UNINSTALLATION

It is recommended to use your distribution's relevant package management
utilities, unless you installed manually or ran into uninstallation
issues.

Grab a copy of autojump:

    git clone git://github.com/joelthelion/autojump.git

Run the uninstallation script:

    cd autojump
    ./uninstall.sh

and follow on screen instructions.

If you keep getting `autojump: command not found` at the prompt,
do:`unset PROMPT_COMMAND`. You can also restart your shell.