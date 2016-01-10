---
title: 2009 hardware purchase proposal
---

Proposal to purchase new machines for OBF
=========================================

Justification
-------------

-   It is imperative that we move to x86\_64 so we can do better support
    of modern hardware
-   Need to upgrade to more modern kernels and OS
-   Propose to stay with CentOS (?)

Proposed purchases
------------------

-   A new machine to replace Portal which would be Xen enabled and
    virtually support mailing lists, web wiki.
-   A new machine to replace dev which would be Xen enabled? and support
    SVN, GIT(?)
-   *Chris to insert price quote(s) and specs here*

Deployment and upgrade plan
---------------------------

-   Decomission old machines, helps free up **donated** rackspace from
    BioTeam
-   Setting up worldwide mirrors for backup purposes (rsync scripts from
    the repository?)
    -   Our 2 most valuable components are src code and mailing list
        (archives and membership). Losing these or being down is a
        HUGE problem. Can we insure these are protected and redundantly
        preserved?
-   How can we balancing security, all volunteer sysadmin team, moderate
    latency in response to issues (due to all volunteer nature)

Community requests
==================

-   Latest and greatest src code tools - GIT/Mercurial, previously Trac
    was also requested.
    -   Has been problematic to support because we currently don't allow
        HTTP access to dev machine
    -   Can we setup NFS + httpd on separate machine with mirrored
        FS (read-only) or NFS(read-write) or other system?
-   How do we keep Wiki's up-to-date w software - better wikifarm
    support?

