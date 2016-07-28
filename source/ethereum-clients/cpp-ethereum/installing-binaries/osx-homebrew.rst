
OS X Homebrew packages
--------------------------------------------------------------------------------

We generate Homebrew packages within our automated build system.

We **only** support the two most recent OS X versions:

- `OS X Yosemite (10.10) <https://en.wikipedia.org/wiki/OS_X_Yosemite>`_
- `OS X El Capitan (10.11) <https://en.wikipedia.org/wiki/OS_X_El_Capitan>`_

**We only support 64-bit builds.**

If your system does not support either of these OS X versions then you
are out of luck.  Sorry!

All OS X builds require you to `install the Homebrew <http://brew.sh>`_
package manager before doing anything else.  Here's how to `uninstall Homebrew
<https://github.com/Homebrew/homebrew/blob/master/share/doc/homebrew/FAQ.md#how-do-i-uninstall-homebrew>`_,
if you ever want to start again from scratch.  

To install the Expanse C++ components from Homebrew, execute these commands: ::

    brew update
    brew upgrade
    brew tap expanse/expanse
    brew install cpp-expanse
    brew linkapps cpp-expanse

Or ... ::

    brew install cpp-expanse --with-gui

... if you want to build
`AlethZero <https://github.com/expanse-org/alethzero>`_ and
the `Mix IDE <https://github.com/expanse-org/wiki/wiki/Mix:-The-DApp-IDE>`_ too.

To start the applications, type one of these commands in a Terminal window: ::

    open /Applications/AlethZero.app
    open /Applications/Mix.app
    eth

Here is the `Homebrew Formula
<https://github.com/expanse-org/homebrew-expanse/blob/master/cpp-expanse.rb>`_
which details all the supported command-line options.
