---
title: SourceCode
---

Anonymous access to the latest hosted source code repositories
==============================================================

This page documents the process of obtaining anonymous CVS or RSYNC
based access to the source code repositories belonging to the Open
Bioinformatics Foundation.

How to browse our latest source code repositories via the web
-------------------------------------------------------------

<http://code.open-bio.org/cgi/viewcvs.cgi>

Downloading and updating code via Anonymous CVS
-----------------------------------------------

(1) Make sure that CVS is installed on your system.

(2) Pick the repository that you wish to use

`   * /home/repository/biopython`  
`   * /home/repository/biojava`  
`   * /home/repository/bioperl`  
`   * /home/repository/biodas`  
`   * /home/repository/moby`  
`   * /home/repository/biocorba`  
`   * /home/repository/biosql`  
`   * /home/repository/bioruby`  
`   * /home/repository/emboss`  
`   * /home/repository/obf-common `

(3) Use the following command (all on one line) to login to the server.

The example below shows how to login to the bioperl repository. To login
to other repositories simply alter the /home/repository/(project)
information.

`   cvs -d :pserver:cvs@cvs.open-bio.org:/home/repository/bioperl login`  
`   when prompted, the password is 'cvs'`

(4) Each project CVS repository can have many different packages
available for download. You may need to browse the web interface for a
bit to determine the packages of interest. After a successful login you
may "checkout" the project package you are interested in.

The following command should be executed as one line. The specific
example shows how to check out the primary bioperl codebase which is
contained in the "bioperl-live" package.

`   cvs -d :pserver:cvs@cvs.open-bio.org:/home/repository/bioperl checkout bioperl-live`

The login and checkout procedure should only have to be done once. To
update the source directories in the future it should be possible just
to enter the top level directory and issue the following command:

`   cvs update`
