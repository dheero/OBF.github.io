---
title: SVN-Developers
---

SVN repository access for developers
====================================

This page is for open-bio affiliated developers who are making use of
SVN based version control systems rather than the traditional CVS based
systems.

Access methods
--------------

### svnserve operates in tunnel mode only

For security and access control reasons we are not running a daemonized
svnserver process or allowing access via HTTP through the Apache
mod\_DAV/svn module methods. The SVN access method that fits best with
our current developer and security model is to run svnserver in "tunnel"
mode on a per-user basis. This means developers will connect and
authenticate via encrypted SSH sessions before svnserver is invoked. In
this scenario svnserver is launched in tunnel mode and runs <em>as the
user who invoked it</em>.

Hosted repositories
-------------------

### blipkit

Blipkit access is achieved via methods such as this:

    svn checkout svn+ssh://dev.open-bio.org/home/svn-repositories/blipkit

Additional SVN documentation
----------------------------

[| Version Control with
SVN](http://svnbook.red-bean.com/en/1.1/index.html)
