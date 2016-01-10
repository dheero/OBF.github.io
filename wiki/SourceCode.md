---
title: SourceCode
---

Anonymous access to the latest hosted source code repositories
==============================================================

This page documents the process of obtaining anonymous [
CVS](wp:Concurrent_Versions_System "wikilink"), [
SVN](wp:SVN "wikilink") or [ RSYNC](wp:Rsync "wikilink") based access to
the source code repositories hosted by the Open Bioinformatics
Foundation. These methods are useful for obtaining cutting edge
sourcecode and developer snapshots.

Note to casual users
--------------------

The methods described here grant access to live snapshots of our current
code repositories. The files may be in constant flux and certainly do
not reflect official packages and supported releases.

For downloads of tested and released software, please visit the official
[Projects](Projects "wikilink") page for links to the project websites
and download locations.

Note to developers
------------------

This page describes methods for obtaining **read only** access to the
latest snapshots of our source code. Updates, fixes and new code **can
not** be committed or uploaded using the methods described here.

How to browse our latest source code repositories via the web
-------------------------------------------------------------

Projects using CVS repositories:
<http://code.open-bio.org/cgi/viewcvs.cgi>

Projects using Subversion repositories:
<http://code.open-bio.org/svnweb/>

Downloading and updating code via Anonymous CVS
-----------------------------------------------

-   Make sure that [ CVS](wp:Concurrent_Versions_System "wikilink") is
    installed on your system.
-   Pick the repository that you wish to use

'''IMPORTANT NOTE (Starting in 2008): BioPerl and BioJava are switching
from CVS to Subversion for source code version control management. At
some point the CVS links below for BioPerl and BioJava will be removed.
'''

`   * `[`/home/repository/biopython`](http://code.open-bio.org/cgi/viewcvs.cgi/?cvsroot=biopython)  
`   * `[`/home/repository/biojava`](http://code.open-bio.org/cgi/viewcvs.cgi/?cvsroot=biojava)  
`   * `[`/home/repository/bioperl`](http://code.open-bio.org/cgi/viewcvs.cgi/?cvsroot=bioperl)  
`   * `[`/home/repository/biodas`](http://code.open-bio.org/cgi/viewcvs.cgi/?cvsroot=biodas)  
`   * `[`/home/repository/moby`](http://code.open-bio.org/cgi/viewcvs.cgi/?cvsroot=biomoby)  
`   * `[`/home/repository/biocorba`](http://code.open-bio.org/cgi/viewcvs.cgi/?cvsroot=biocorba)  
`   * `[`/home/repository/biosql`](http://code.open-bio.org/cgi/viewcvs.cgi/?cvsroot=biosql)  
`   * `[`/home/repository/bioruby`](http://code.open-bio.org/cgi/viewcvs.cgi/?cvsroot=bioruby)  
`   * `[`/home/repository/emboss`](http://code.open-bio.org/cgi/viewcvs.cgi/?cvsroot=emboss)  
`   * `[`/home/repository/obf-common`](http://code.open-bio.org/cgi/viewcvs.cgi/?cvsroot=obf-common)` `

-   Use the following command (all on one line) to login to the server.
    The example below shows how to login to the bioperl repository. To
    login to other repositories simply alter
    the /home/repository/(project) information.

`   cvs -d :pserver:cvs@code.open-bio.org:/home/repository/bioperl login`

-   When prompted, the password is 'cvs'
-   Each project CVS repository can have many different packages
    available for download. You may need to browse the web interface for
    a bit to determine the packages of interest. After a successful
    login you may "checkout" the project package you are interested in.

The following command should be executed as one line. The specific
example shows how to check out the primary bioperl codebase which is
contained in the "bioperl-live" package.

`   cvs -d :pserver:cvs@code.open-bio.org:/home/repository/bioperl checkout bioperl-live`

-   The login and checkout procedure should only have to be done once.
    To update the source directories in the future it should be possible
    just to enter the top level directory and issue the following
    command:

`   cvs update`

Downloading and updating code via Anonymous Rsync
-------------------------------------------------

The code.open-bio.org server also offers up read-only copies of source
code repositories via anonymous [ rsync](wp:Rsync "wikilink").

To see a list of available rsync modules, try this command:

` rsync `[`rsync://code.open-bio.org`](rsync://code.open-bio.org)

The server will echo back the list of configured repositories. The
module name is appended to the "::" pattern to indicate to the rsync
server that a module is being requested.

The following example shows how to obtain the latest Bioperl codebase
snapshot using anonymous rsync:

` rsync -av code.open-bio.org::cvsbioperl .`

Downloading and updating code via Anonymous SVN
-----------------------------------------------

The code.open-bio.org server also offers up read-only copies of source
code repositories via anonymous [ SVN](wp:SVN "wikilink"). A list of
code repositories available via SVN can be seen here:
<http://code.open-bio.org/svnweb/index.cgi>

*Example Usage*:

To see what SVN modules the BioJava project is making available, try
this command:

` svn list `[`svn://code.open-bio.org/biojava`](svn://code.open-bio.org/biojava)

The following example shows how to obtain the latest Bioperl codebase
snapshot using anonymous SVN, it will check out the latest copy of
bioperl-live/ from the "SVN trunk" and will locally store it in a
directory named "bioperl-live" on your system:

` svn co `[`svn://code.open-bio.org/bioperl/bioperl-live/trunk`](svn://code.open-bio.org/bioperl/bioperl-live/trunk)` bioperl-live`
