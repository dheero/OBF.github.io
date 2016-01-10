---
title: 2009 hardware purchase proposal
---

Proposal to purchase new machines for OBF
=========================================

Justification
-------------

**Total Server Refresh - Move to 100% hypervisor-based virtualization**

-   Existing servers date back to 2004 and are based on 32bit Pentium 4
    chipsets
-   Existing servers running CentOS 4.8, current CentOS is at version
    5.4
-   No spare server capacity for new service and server requests from
    OBF community
-   Only two people (Chris D and Jason S) have 100% full remote control
    including remote-power reboot ability
    -   Can not easily/securely provide full remote control to other
        volunteers with existing infrastructure
-   We need to move to 64 bits, x86\_64 and take advantage of CPU level
    support for virtulization
-   Virtualizing our servers and services greatly reduces operational
    burden, makes our IT infrastructure more "portable" should future
    situations demand it and also solves much of our existing issues
    with granting high levels of remote admin access (including console
    & remote power control) to members of our sysadmin team
-   New 64-bit hardware with CPU level virtualization support would
    allow OBF to:
    -   Run many more servers and services as needed
    -   Provide higher levels of performance
    -   Provide higher levels of redundancy, safety and portability
    -   Allow much greater distribution of administrative powers
    -   Consume less datacenter space
    -   Consume less datacenter electricity

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

