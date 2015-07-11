# hiss

HISS is the Haskell Interface for Simple Syndication, an RSS reader
written in Haskell.

## Installation
As [cabal is not a package manager][cabal], it is recommended not to install
**hiss** directly through cabal.  Instead, you should follow this workflow:

~~~bash
mkdir -p ~/install/hiss
git clone https://github.com/adituv/hiss ~/install/hiss
cd ~/install/hiss
cabal sandbox init
cabal install hiss
sudo ln -s ./.cabal-sandbox/bin/hiss /usr/bin/hiss
~~~

This installs **hiss** and all its dependencies independently of any any other
haskell packages, removing the chance of conflicts (excluding the possibility
of incorrect cabal configuration files), then creates a link from the installed executable of **hiss** in the /usr/bin directory.

## Updating
Once a copy of **hiss** is on your system, you can update it as so:

~~~bash
cd ~/install/hiss
git pull origin master
cabal install
~~~

[cabal]: https://ivanmiljenovic.wordpress.com/2010/03/15/repeat-after-me-cabal-is-not-a-package-manager/
