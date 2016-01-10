---
title: EU Codefest 2012
---

EU-codefest 2012 was 19 and 20 July in Lodi Italy
=================================================

In coordination with the [BOSC](BOSC "wikilink") committee we organised
the first EU-Codefest, a low-key event the week after [BOSC
2012](BOSC_2012 "wikilink") in California.

15 people attended the EU-Codefest, which took place on 19 and 20 July
2012, in [Lodi,
Italy](http://www.openstreetmap.org/?lat=45.31&lon=9.508&zoom=10&layers=M),
near Bergamo and Milano.

The EU-Codefest is modeled on the successful biohackathons in Japan,
though we like it more free-flowing.

The weekend after 21 and 22 July continued (unofficially) to have a good
time, and organised some outings.

Organising committee: Francesco Strozzi, Raoul Bonnal and Pjotr Prins

Location
--------

[Parco Tecnologico Padano](http://www.tecnoparco.org/) vie Einstein -
Loc. Cascina Codazza 26900,
[Lodi](http://www.openstreetmap.org/?lat=45.31&lon=9.508&zoom=10&layers=M)
- ITALY

Topics
------

Three main topics were worked on during the CodeFest:

-   NGS and high performance parsers for OpenBio projects.
-   RDF and semantic web for bioinformatics.
-   Bioinformatics pipelines definition, execution and distribution.

During the conference we discussed current issues and added

-   Service discovery and integration (Debian, BioMoby,
    biogems.info, BioLinux)
-   Workflow (bio-ngs, Galaxy, Taverna)
-   PBS (bio-ngs)
-   Software
    -   bio-ngs
    -   bio-maf introducing into pipeline
    -   gff3
    -   biogems.info (Debian packages)
    -   bio-table (RDF support)
    -   biowsr

Talks
-----

The following talks/introductions/micro-presentations were given at the
Codefest:

-   *Semantic Web for the Integrated Genomic Data* by Toshiaki Katayama,
    Database Center for Life Science, Tokyo, Japan
-   *Writing the worlds fastest GFF3 parser* by Marjan Povolni, Faculty
    of Technical Sciences Novi Sad, Serbia
-   *Debian packaging* by Steffen Möller, University of Lübeck, Germany
-   *BioWSR Bioinformatic Web Services Registry project update* by José
    María Fernández González, Protein Design Group, CNB-CSIC
    Cantoblanco, Madrid,

Spain

-   *RNA-seq project introduction* by James Tojo, Karolinska University,
    Stockholm, Sweden
-   *Software resources for Bioinformatics, including
    <http://biogems.info/>* by Pjotr Prins, Wageningen University, The
    Netherlands

Reports
-------

### Bio-ngs

We worked on developing bio-ngs to better handle pipelines and
reproducible workflows, plus semantic databases to manage and query NGS
sec ondary analysis data.

### Bio RDF support

During the codefest we discussed the ins- and outs of graph stores, and
the semantic web (triple stores). We now share a vision on how to move
forward, using RDF for biological analysis. The next biohackathon will
be in Japan in September 2012. Four of us will be there to continue this
work.

### Adding a list of BioLinux Software packages to biogems.info

We recognise is it often hard to find relevant information on current
software packages. At the USA codefest, a week earlier, Brad Chapman and
Hervé Ménager created a Manifest of bioinformatics packages installed on
a running CloudBiolinux system (VM). At the EU codefest a web
representation was created that parsed the manifest, pulled some more
information from the Debian package information and generates the page
<http://www.biogems.info/biolinux.html>.

The new overview led to a discussion on BioLinux/Debian packaging:

The overview helps the different parties focus on priorities (with
packaging software).

Brad writes: From the Debian/Bio-Linux/packaging side, I'm happy to
modify where we pull packages from. The goal is to have everything in
single repositories to be community maintained so I'm similarly happy if
some of the CloudBioLinux specific builds pick up package maintainers.
The (CloudBiolunx) custom scripts now are there of necessity and not
meant to be permanent. I'm also digging into nix so if there are any
packages there that we've missed and would be useful, we can move that
direction as well. It was also noted that proper Debian packages also
track popularity statistics (based on installation of Debian).

Steffen added: My general concern (and motivation) is community forming
and an avoidance of redundancies. That is why a nice friendly embracing
email sent to the Debian/Ubuntu folks on Debian Med I consider
important. Your efforts should be perceived as a continuation of the
Debian Med efforts, not as a competition.

### BioWSR

In bioinformatics, and in general life sciences, there are plenty of web
services built following the different web service paradigms and
bioinformatic web service variants: REST , SOAP, BioMOBY\[1\], DAS\[2\],
BioMart\[3\], etc... Although there are already web service repositories
like BioMOBY and web service catalogues like BioCatalogue\[4\] or
DASRegistry\[5\], we feel that many of the existing solutions are not
extensible enough to be applied to new web service paradigms. Even
worse, in some cases the source code of the registry is not available,
so it cannot be reused, improved or extended.

So we (at INB) started the design and implementation of a new web
service repository (in Ruby) that will allow us (and anyone using the
codebase we are developing) to document and manage the web services
developed by different groups, being open and extensible to the entire
range of web service paradigms and variants used in bioinformatics. Due
to the large web service portfolio the INB possesses, one of the main
concerns when designing BioWSR was that web services from any paradigm
should be describable at a certain level. As the new registry is
strongly inspired by the BioMOBY repository, one requisite was that RDF
triples should be a superset of the ones used in BioMOBY to make it
backward compatible.

### GFF3/GTF tools

During the codefest we collected info on what requirements are there for
GFF3/GTF tools, and worked on Debian packages for the same tools

### Debian packaging

We introduced a few people to Debian packaging and key signing. For
CloudBiolinux we encourage further Debian packaging of both BioLinux
packages, and custom build scripts. It was noted, for example, that
Debian has a more recent version of Jalview than the biolinux-jalview
package.

### RNA-seq visualisation

We were working on NGS, more specifically looking to our RNA sequencing
project... Just wanted to check with you guys if everyone follows the
same methods/pipeline for RNA sequencing. Also managed to set up
Gbrowser with help of Paulo for our RNA seq project and also looked to
other visualization tools. Meeting you guys and learning from the group
was really helpful. Now I have a feeling to work on some of the open
source projects but I guess I need to learn bit more to reach that
level.
