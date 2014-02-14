---
title: Google Summer of Code 2014 Ideas
---

The details of each of our project ideas are listed below, including
potential mentors. Interested mentors and students should subscribe to
the OBF/GSoC [mailing
list](http://lists.open-bio.org/mailman/listinfo/gsoc) and announce
their interest.

See the main OBF [Google Summer of
Code](Google_Summer_of_Code "wikilink") page for more information about
the GSoC program and additional ways to get in touch with us.

Cross-project ideas
-------------------

### BioInterchange: Convert and Exchange Biological File Formants using RESTful web service

Rationale  
[BioInterchange](http://www.biointerchange.org/index.html) Interchange
data using the Resource Description Framework (RDF) and let
BioInterchange automagically create RDF triples from your TSV, XML,
GFF3, GVF, Newick and other files common in Bioinformatics.
BioInterchange helps you transform your data sets into linked data for
sharing and data integration via command line, web-service, or API.
BioInterchange was conceived and designed during NBDC/DBCLS's
[BioHackathon 2012](http://2012.biohackathon.org/). Architecture and RDF
serialization implementations were provided by Joachim Baran, Geraint
Duck provided JSON and XML deserialization implementations and
contributed to architecture decisions, guidance on ontology use and
applications were given by Kevin B. Cohen and Michel Dumontier, where
Michel brought forward and extended the Semanticscience Integrated
Ontology (SIO). Jin-Dong Kim helped to define ontology relationships for
RDFizing DBCLS' PubAnnotation category annotations. The main idea is to
have a central service with can be used as a validator and as
interchange service for different languages.

<!-- -->

Approach  
The project will identify the most common and used file formants for all
the currently used language under OBF and will design a RESTful API and
will project an implementation for all the supported languages.
BioInterchange was developed with Ruby but the scope of the project is
to have an agnostic system which let use implement a converter using the
best language for that functionality. It expected to have a high traffic
for the service so an appropriate refactoring or reimplementation using
parallel techniques or languages devoted to parallel programming would
be possible.

<!-- -->

Difficulty and needed skills  
The project is mid / high difficulty, aimed at talented students.
Previous knowledge of Ruby or other scripting language is preferred and
flexibility in learning other languages is requireed.

The project requires  
Knowledge of advanced programming languages and meta-programming and
some concept in parallelizing and web services design.

<!-- -->

Mentors  
Raoul J.P. Bonnal, Francesco Strozzi, Toshiaki Katayama, Joachim Baran

### Language APIs for the Systems Biology Markup Language (SBML) through the JVM

Rationale  
The standard Java implementation of SBML, JSBML, is used as a parser for
various Java-based systems biology applications.

This fulfills one niche, but the versatility of the JVM can be utilized
to employ JSBML as a parser for systems biology applications that are
written in other languages. Also, JSBML undergoes an active community
effort to be up-to-date with current SBML standards.

Approach  
This project will aim to present language APIs for languages that may
want to employ the SBML structure without building a parser
from scratch. Matlab, Mathematica, and Python APIs will be the focus for
this project.

<!-- -->

Languages and skill  
Java, optional: Matlab, Python, (other language)

<!-- -->

Mentors  
Andreas Dräger, Alex Thomas

[BioPerl](http://bioperl.org/wiki/Google_Summer_of_Code)
--------------------------------------------------------

![](BioPerl_logo_tiny.jpg "BioPerl_logo_tiny.jpg")

-   **[ BioPerl GSoC Page](bp:Google_Summer_of_Code "wikilink")** -
    project ideas and mentors
-   [Project website](bp:Main_Page "wikilink")
-   [Information for new developers](bp:Becoming_a_developer "wikilink")
-   source code browser for
    [bioperl-live](http://code.open-bio.org/svnweb/index.cgi/bioperl/browse/bioperl-live/trunk)
    (the main BioPerl code base), and [all BioPerl
    sub-projects](http://code.open-bio.org/svnweb/index.cgi/bioperl/)
-   [Priority list](bp:Project_priority_list "wikilink") of things that
    need work, as another source for student-conceived project ideas
-   [Mailing lists](bp:Mailing_lists "wikilink")
-   IRC: `#bioperl` on [Freenode](http://freenode.net)

### [NGS-friendly BioPerl code](http://bioperl.org/wiki/Google_Summer_of_Code#NGS-friendly_BioPerl_code)

### \[<http://bioperl.org/wiki/Google_Summer_of_Code#Convert_BioPerl-DB_to_DBIx>::Class Convert BioPerl-DB to use DBIx::Class\]

### [Major BioPerl Reorganization (Part II)](http://bioperl.org/wiki/Google_Summer_of_Code#Major_BioPerl_Reorganization.2C_part_2)

### [Perl Run Wrappers for External Programs in a Flash](http://bioperl.org/wiki/Google_Summer_of_Code#Perl_Run_Wrappers_for_External_Programs_in_a_Flash)

### [Lightweight BioPerl modules](http://bioperl.org/wiki/Google_Summer_of_Code#Lightweight.2FLazy_BioPerl_Classes)

### [Modern BioPerl: BioPerl 2.0 and beyond](http://bioperl.org/wiki/Google_Summer_of_Code#BioPerl_2.0_.28and_beyond.29)

### \[<http://bioperl.org/wiki/Google_Summer_of_Code#Bio>::Assembly Bio::Assembly\]

### [Semantic Web Support](http://bioperl.org/wiki/Google_Summer_of_Code#Semantic_Web_Support)

[BioJava](http://biojava.org/wiki/Google_Summer_of_Code)
--------------------------------------------------------

![](Biojava_logo_tiny.jpg "Biojava_logo_tiny.jpg")

-   **[BioJava GSoC
    Page](http://biojava.org/wiki/Google_Summer_of_Code)** - project
    ideas and mentors
-   [BioJava modules](http://biojava.org/wiki/BioJava:Modules) as
    another source for student-conceived project ideas
-   source code for
    [biojava-live](http://code.open-bio.org/svnweb/index.cgi/biojava/browse/biojava-live/trunk)
    (the main BioJava code base) and [all BioJava
    sub-projects](http://code.open-bio.org/svnweb/index.cgi/biojava/)
-   [Mailing lists](http://biojava.org/wiki/BioJava:MailingLists)
-   No IRC channel at present

### JVM support and improvements for the Systems Biology Markup Language

See [Native and JVM-based support for the Systems Biology Markup
Language (SMBL)](http://sbml.org/GSoC2014)

[BioPython](biopython:Google_Summer_of_Code "wikilink")
-------------------------------------------------------

![](Biopython_logo_tiny.png "Biopython_logo_tiny.png")

-   **[ BioPython GSoC
    Page](biopython:Google_Summer_of_Code "wikilink")** - project ideas
    and mentors
-   [Project website](biopython:Main_Page "wikilink")
-   [Information for contributors](biopython:Contributing "wikilink")
-   [Mailing lists](biopython:Mailing_lists "wikilink")
-   [ Source Code](biopython:SourceCode "wikilink")
-   No IRC channel at present

### [Indexing & Lazy-loading Sequence Parsers](http://biopython.org/wiki/Google_Summer_of_Code#Indexing_.26_Lazy-loading_Sequence_Parsers)

[BioRuby](http://bioruby.open-bio.org/wiki/Google_Summer_of_Code)
-----------------------------------------------------------------

![](BioRuby_logo_tiny.png "BioRuby_logo_tiny.png")

-   **[BioRuby GSoC
    Page](http://bioruby.open-bio.org/wiki/Google_Summer_of_Code)** -
    project ideas and mentors
-   [Project website](http://bioruby.org)
-   [developers mailing
    list](http://lists.open-bio.org/mailman/listinfo/bioruby)
-   [source code](http://github.com/bioruby/bioruby/tree/master)
-   IRC: `#bioruby` on [Freenode](http://freenode.net)

### [An ultra-fast scalable RESTful API to query large numbers of genomic variations](http://bioruby.open-bio.org/wiki/Google_Summer_of_Code#An_ultra-fast_scalable_RESTful_API_to_query_large_numbers_of_genomic_variations)

[BioHaskell](http://biohaskell.org/Google_Summer_of_Code)
---------------------------------------------------------

:\* [Project website](http://biohaskell.org/)

:\* [Bioinformatics section on
HackageDB](http://hackage.haskell.org/packages/#cat:Bioinformatics)

### [Optimizing a novel, very sensitive alignment method](http://biohaskell.org/Google_Summer_of_Code#Optimizing_transalign)
