---
title: Google Summer of Code 2015 Ideas
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

OBF is an umbrella organization which represents many different
programming languages used in
[bioinformatics](http://en.wikipedia.org/wiki/Bioinformatics). In
addition to working with each of the "Bio\*" projects (listed below),
this year we are also accepting a category of "cross-project" ideas that
cover multiple programming languages or projects. These collaborative
ideas are broadly defined and can be thought of as "unfinished" —
interested students should adapt the ideas to their own strengths and
goals, and are responsible for the quality of the final proposed idea in
their application.

**Feel free to propose your own entirely new idea**. You can also draw
ideas from [Genome Informatics
(GMOD)](http://gmod.org/wiki/GSoC#2014_Project_Ideas) and the [National
Evolutionary Synthesis Center
(NESCent)](http://informatics.nescent.org/wiki/Phyloinformatics_Summer_of_Code_2014).

### Provide Nextflow with a GUI based on NoFlo UI

Rationale  

Nextflow is a data-driven toolkit for computational pipelines that
simplify writing parallel and scalable pipelines in a portable manner.
Its goal is to make data analysis required by next generation sequence
technologies and, in more general terms, bioinformatics applications
easier for researchers.

  

It follows the UNIX philosophy where many small tools can be composed
together to create efficient computational solutions where individual
parts can be easily replaced. It has been designed to allow developers
to fast prototype applications reusing their existing tools and scripts.
For this reason it has been developed primarily as a command line
oriented tool. However, complex pipelines may benefit from having a
visualisation layer that helps the developer design and represent the
application workflow logic.

  

NoFlo-UI is the presentation layer for NoFlo, a flow-based programming
(FBP) environment that makes software creation more accessible and
collaborative. It provides an interactive interface which allows you to
create a computational workflow by dragging, dropping and connecting the
different task components. It basically allows you to "draw" an
application in such a way that it resembles a subway map. This "map" can
then be more easily understood, shared and curated by other scientists,
compared to managing endless files of source code.

Approach  

The goal, therefore, of the this proposal is to implement a graphical
front-end, based on the NoFlo-UI project, for the Nextflow programming
environment. This would provide the latter with a presentation layer
that would allow researchers to "sketch" their computational pipelines
instead of programming them, making it easier to share and handle
complex task interactions in their application logic.

  

Ideally this integration will implement a two-way tool in such a way
that changes, applied in the visual editor, are reflected in the
Nextflow scripting language and vice-versa.

Languages and skills  

The student is required to have proven working ability with Javascript,
HTML5, Polymer and Node.js for the front-end development and good level
of knowledge of the Groovy/Java programming languages for Nextflow side.
He/she may also benefit by having some theoretical and practical
knowledge of programming language syntax and grammar parsers.

Code  

Nextflow source code is available at the following repository
(https://github.com/nextflow-io/nextflow/) NoFlo-UI source code is
available at this link (https://github.com/noflo/noflo-ui/)

Mentors  

Paolo Di Tommaso

### Low latency scheduling and in-memory data processing

Rationale  
Nextflow does not implement a task scheduling strategy on its own and

delegates it to the underlying processing infrastructure, which in most
cases is a grid engine like technology. However these platforms were
designed for job processing in a batch scheduling fashion, i.e few long
duration jobs scheduled sequentially to the computer-cluster facility.
This approach suffers of very high latencies that makes it unfit to
highly parallel and short-lived jobs that are more and more commons in
bioinformatics data analysis.

Approach  
The goal of this proposal is integrating Sparrow scheduler (

<https://github.com/radlab/sparrow>) and Tachyon in-memory file system (
<https://github.com/amplab/tachyon>) with Nextflow.

The first is a high throughput, low latency distributed cluster
scheduler, while the second is a memory centric distributed file system.
Both of them are open source research project developed at UC Berkeley.

The integration of these technologies would allow Nextflow to manage
large distributed workloads in a more efficient and timely manner, to
decrease tasks granularity in Nextflow applications, gaining an higher
parallelism degree and better applications performance.

Languages and skill  
TEXT HERE TEXT HERE

<!-- -->

Code  
TEXT HERE TEXT HERE

<!-- -->

Mentors  
TEXT HERE TEXT HERE

### TITLE

Rationale  
TEXT HERE TEXT HERE

<!-- -->

Approach  
TEXT HERE TEXT HERE

<!-- -->

Languages and skill  
TEXT HERE TEXT HERE

<!-- -->

Code  
TEXT HERE TEXT HERE

<!-- -->

Mentors  
TEXT HERE TEXT HERE

[BioPerl](http://bioperl.org/wiki/Google_Summer_of_Code)
--------------------------------------------------------

![](BioPerl_logo_tiny.jpg "BioPerl_logo_tiny.jpg")

-   [Mailing lists](bp:Mailing_lists "wikilink")
-   IRC: `#bioperl` on [Freenode](http://freenode.net)
-   [Information for new developers](bp:Becoming_a_developer "wikilink")
-   Source code browser for
    [bioperl-live](https://github.com/bioperl/bioperl-live) (the main
    BioPerl code base), and [all BioPerl
    sub-projects](https://github.com/bioperl)
-   [Priority list](bp:Project_priority_list "wikilink") of things that
    need work, as another source for student-conceived project ideas

### TITLE

Rationale  
TEXT HERE TEXT HERE

<!-- -->

Approach  
TEXT HERE TEXT HERE

<!-- -->

Languages and skill  
TEXT HERE TEXT HERE

<!-- -->

Code  
TEXT HERE TEXT HERE

<!-- -->

Mentors  
TEXT HERE TEXT HERE

[BioJava](http://biojava.org/wiki/Google_Summer_of_Code) and JSBML
------------------------------------------------------------------

![](Biojava_logo_tiny.jpg "Biojava_logo_tiny.jpg")

-   [BioJava developer mailing
    list](http://lists.open-bio.org/mailman/listinfo/biojava-dev)
-   [JSBML developer mailing
    list](https://groups.google.com/forum/#!forum/jsbml-development)
-   [BioJava modules](http://biojava.org/wiki/BioJava:Modules) as
    another source for student-conceived project ideas
-   Source code for
    [biojava-live](http://code.open-bio.org/svnweb/index.cgi/biojava/browse/biojava-live/trunk)
    (the main BioJava code base) and [all BioJava
    sub-projects](http://code.open-bio.org/svnweb/index.cgi/biojava/)

For GSoC 2014, BioJava is partnering with the Systems Biology Markup
Language (SMBL) team to bring enhancements to JSBML, the standard Java
implementation of SBML, and bring SBML features to other Java-based
systems biology software. See [the SMBL
website](http://sbml.org/GSoC2014) for more ideas from the SBML team.

Students working on these projects will interact with both the BioJava
and JSBML communities, which overlap. Most development will happen on
the JSBML codebase, although BioJava is used as a supporting library for
some components.

### TITLE

Rationale  
TEXT HERE TEXT HERE

<!-- -->

Approach  
TEXT HERE TEXT HERE

<!-- -->

Languages and skill  
TEXT HERE TEXT HERE

<!-- -->

Code  
TEXT HERE TEXT HERE

<!-- -->

Mentors  
TEXT HERE TEXT HERE

[BioPython](biopython:Google_Summer_of_Code "wikilink")
-------------------------------------------------------

![](Biopython_logo_tiny.png "Biopython_logo_tiny.png")

-   [Mailing lists](biopython:Mailing_lists "wikilink")
-   [Information for contributors](biopython:Contributing "wikilink")
-   [ Source Code](biopython:SourceCode "wikilink")

### TITLE

Rationale  
TEXT HERE TEXT HERE

<!-- -->

Approach  
TEXT HERE TEXT HERE

<!-- -->

Languages and skill  
TEXT HERE TEXT HERE

<!-- -->

Code  
TEXT HERE TEXT HERE

<!-- -->

Mentors  
TEXT HERE TEXT HERE

[BioRuby](http://bioruby.open-bio.org/wiki/Google_Summer_of_Code)
-----------------------------------------------------------------

![](BioRuby_logo_tiny.png "BioRuby_logo_tiny.png")

-   [Developers mailing
    list](http://lists.open-bio.org/mailman/listinfo/bioruby)
-   [Source code](http://github.com/bioruby/bioruby/tree/master)
-   IRC: `#bioruby` on [Freenode](http://freenode.net)

### TITLE

Rationale  
TEXT HERE TEXT HERE

<!-- -->

Approach  
TEXT HERE TEXT HERE

<!-- -->

Languages and skill  
TEXT HERE TEXT HERE

<!-- -->

Code  
TEXT HERE TEXT HERE

<!-- -->

Mentors  
TEXT HERE TEXT HERE

[BioHaskell](http://biohaskell.org/Google_Summer_of_Code)
---------------------------------------------------------

:\* [Project website](http://biohaskell.org/)

:\* [Bioinformatics section on
HackageDB](http://hackage.haskell.org/packages/#cat:Bioinformatics)

:\* [GSoC page](http://biohaskell.org/Google_Summer_of_Code)

Biohaskell has its own gsoc page. We currently have 2 (+1) open problems
listed there. In addition, we accept peoples' own ideas and have a
number of open problems not listed. The latter fall somewhere between
bachelors thesis and PhD work and are harder to nicely package up.

### Fast k-mer indexing

Fast k-mer indexing requires a data structure mapping a short string of
k characters to a value. While trivial to do with almost all key-value
maps, we also require a very memory-efficient storage system. Knowledge
of suffix structures is a definite plus.

Mentors  
Ketil Malde?

### Low-level bit and stream-fusion optimizations

In Haskell, we typically don't talk that much about low-level
implementation details. For some algorithms, low-level details
(especially bitwise operations and SIMD instructions) become important.
I have a library dealing with bitsets but it is not yet fully efficient.
Getting SIMD instructions to play nice with /generic/ DP recursion
schemes is probably really hard.

Mentors  
Christian Hoener zu Siederdissen

[Biocaml](http://biocaml.org)
-----------------------------

:\* [Mailing List](https://groups.google.com/d/forum/biocaml)

### TITLE

Rationale  
TEXT HERE TEXT HERE

<!-- -->

Approach  
TEXT HERE TEXT HERE

<!-- -->

Languages and skill  
TEXT HERE TEXT HERE

<!-- -->

Code  
TEXT HERE TEXT HERE

<!-- -->

Mentors  
TEXT HERE TEXT HERE

Candidate a new project for OBF
-------------------------------

Please if you want to be part of OBF but you porject is not yet listed
above, contact us and let us know about your project and your proposal.

### TITLE

Rationale  
TEXT HERE TEXT HERE

<!-- -->

Approach  
TEXT HERE TEXT HERE

<!-- -->

Languages and skill  
TEXT HERE TEXT HERE

<!-- -->

Code  
TEXT HERE TEXT HERE

<!-- -->

Mentors  
TEXT HERE TEXT HERE


