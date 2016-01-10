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

### Nextflow graphical front-end

Rationale  
Nextflow is a data-driven toolkit for computational pipelines that
simplify writing parallel and scalable pipelines in a portable manner.
Its goal is to make data analysis required by next generation sequence
technologies and, in more general terms, bioinformatics applications
easier for researchers. You can read more about Nextflow at this
link (http://www.nextflow.io).

<!-- -->

  
It follows the UNIX philosophy where many small tools can be composed
together to create efficient computational solutions where individual
parts can be easily replaced. It has been designed to allow developers
to fast prototype applications reusing their existing tools and scripts.
For this reason it has been developed primarily as a command line
oriented tool. However, complex pipelines may benefit from having a
visualisation layer that helps the developer design and represent the
application workflow logic.

<!-- -->

  
NoFlo-UI is the presentation layer for NoFlo, a flow-based
programming (FBP) environment that makes software creation more
accessible and collaborative. It provides an interactive interface which
allows you to create a computational workflow by dragging, dropping and
connecting the different task components. It basically allows you to
"draw" an application in such a way that it resembles a subway map. This
"map" can then be more easily understood, shared and curated by other
developers, compared to managing endless files of source code.

<!-- -->

Approach  
The goal, therefore, of the this proposal is to implement a graphical
front-end, based on the NoFlo-UI project, for the Nextflow
programming environment. This would provide the latter with a
presentation layer that would allow scientists to "sketch" their
computational pipelines instead of programming them, making it easier to
share and handle complex task interactions in their application logic.

<!-- -->

  
Ideally this integration will implement a two-way tool in such a way
that changes, applied in the visual editor, are reflected in the
Nextflow scripting language and vice-versa.

<!-- -->

Languages and skills  
The student is required to have proven working ability with Javascript,
HTML5, Polymer and Node.js for the front-end development and good level
of knowledge of the Groovy/Java programming languages for Nextflow side.

<!-- -->

  
He/she may also benefit by having some theoretical and practical
knowledge of programming language syntax and grammar parsers.

<!-- -->

Code  
Nextflow source code is available at the following
repository (https://github.com/nextflow-io/nextflow/)

NoFlo-UI source code is available at this
link (https://github.com/noflo/noflo-ui/)

<!-- -->

Mentors  
Paolo Di Tommaso

### Nextflow low latency scheduling and in-memory data processing

Rationale  
Nextflow is a data-driven toolkit for computational pipelines that
simplify writing parallel and scalable pipelines in a portable manner
across different execution platforms. Its goal is to make data analysis
required by next generation sequence technologies and, in more general
terms, bioinformatics applications easier for researchers. You can read
more about Nextflow at this link (http://www.nextflow.io).

<!-- -->

  
Nextflow does not implement a task scheduling strategy on its own but
delegates it to the underlying processing infrastructure, which in most
cases is a grid engine like technology (SGE, PBS, SLURM, etc). However,
these platforms were designed for job processing in a batch scheduling
fashion, i.e. a few long duration jobs scheduled sequentially to the
computer-cluster facility. This model suffers from very high latencies
which make it unfit for highly parallel and short-lived jobs that are
more and more common in bioinformatics data analysis.

<!-- -->

  
The goal of this proposal is to integrate the Sparrow scheduler and
Tachyon in-memory file system with Nextflow to overcome the limitations
of batch-like schedulers generally available in most common cluster
computation facilities.

<!-- -->

  
The first is a high throughput, low latency distributed cluster
scheduler, while the second is a memory centric distributed file system.
Both of them are open source research projects developed at UC Berkeley.

<!-- -->

  
The integration of these technologies would allow Nextflow to manage
large distributed workloads in a more efficient and timely manner and to
decrease the task granularity in Nextflow pipelines. Thus gaining an
higher parallelism degree and better applications performance.

<!-- -->

Approach  
Nextflow implements an extensible mechanism that allows it to support
several computing platforms and file systems in a portable manner.

The approach suggested consists in implementing a new Nextflow executor
which integrates the Sparrow scheduler and its features.

The support for Tachyon file system can be added to Nextflow by writing
an adapter layer that follows the Java JSR-203 specification.

<!-- -->

Languages and skills  
Student is required to have proven working ability with the Java and/or
Groovy programming languages and a good level of theoretical and
practical knowledge in parallel and concurrent programming.

<!-- -->

Code  
Nextflow source code
repository (https://github.com/nextflow-io/nextflow)

Sparrow cluster source code (https://github.com/radlab/sparrow)

Tachyon file system source code (https://github.com/amplab/tachyon)

<!-- -->

Mentors  
Paolo Di Tommaso

### Create GNU Guix Bioinformatics packaging system and add support to CloudBiolinux

Rationale  
[GNU Guix](http://www.gnu.org/software/guix/) is a next generation
software packaging system that has many interesting

features for bioinformatics including multi-version support,
transactional installs and reproducible systems.

GNU GUix is written in the Scheme/LISP programming language and works
well with

virtual machines and Docker, for example.

Currently CloudBiolinux depends on linuxbrew/homebrew for creating
special packages.

We propose to replace part of the linuxbrew infrastructure with that of
GNU Guix.

Having the GNU Guix bionformatics package will allow us to run exactly

the same software on workstations, servers and virtual machines.

<!-- -->

Approach  
Write in Scheme a new collection of bioinformatics packages for GNU Guix
as part of the GNU

project, perhaps adding further support for Ruby and Python interpreters
in the process

(Python is rather well supported already). Embed GNU Guix inside
CloudBiolinux by

using 'flavors'. Also

write a testing infrastructure in Python. Next introduce GNU Guix to
Galaxy as part

of the Galaxy toolshed.

<!-- -->

Languages and skills  
Interest in reproducible software deployment for bioinformatics. Willing
to learn Scheme, some command of Python.

<!-- -->

Code  
GNU Guix presentation at codefest 2014:
<http://www.gnu.org/software/guix/guix-openbio-codefest-20140709.pdf>

GNU Guix source: <http://www.gnu.org/software/guix/>

CloudBiolinux and Galaxy source and info: <http://cloudbiolinux.org/>

<!-- -->

Mailing list  
We will use the CloudBiolinux [mailing
list](https://groups.google.com/forum/#!forum/cloudbiolinux)

Mentors  
Pjotr Prins, Marco van Zwetselaar, Brad Chapman, Dave Thompson

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

### NGS-friendly BioPerl code

Rationale : BioPerl is known to be slow re: any data sets, but particularly when dealing with very large data (e.g. anything related to NGS analysis. Can we make it better? Where should we focus our efforts?  

<!-- -->

Approach : Under the supervision of their mentor(s), the GSoC student will:  

:\* Benchmark bottlenecks that lead to loss in performance for NGS
analyses

:\* Refactor old classes or develop new optimized code for NGS analysis

Challenges : This can be a self-contained project, but will require a lot of discussion on what areas to focus on. Some knowledge of C-based code may be required in cases where low-level library bindings could be generated.  

<!-- -->

Difficulty and needed skills : easy to hard, depending on student's familiarity with the tools to be used. Student will need:  

:\* excellent Perl programming skills, including familiarity with NGS
datasets

\* knowledge of modern Perl practices.  

<!-- -->

Mentors : Chris Fields, Mark Jensen  

### BioPerl 2.0 / BioPerl6

Rationale : Design or reimplement BioPerl classes without API constraint, using Modern Perl tools or Perl 6.  

<!-- -->

Approach 1: A viable Perl6 implementation, Rakudo, is available, with a beta ready to be announced by Sept. and a full Perl6 release by this December 2015. This gives us an enormous opportunity to redesign fundamental aspects of BioPerl without the necessity for development hindered by a requirement for backwards compatibility.  
Approach 2 : Most BioPerl code is over 6 years old and doesn't take advantage of Modern Perl tools, such as new methods in later versions of perl, /MooseX, , and more. Set up the basic core classes that allow mingling of Modern Perl with older BioPerl classes; propose and benchmark variations of specific core classes utilizing Modern Perl tools.  

<!-- -->

Code: Two projects, Biome (Moose-based BioPerl) and BioPerl6 (Perl 6 BioPerl) have already started but are best described as proof of concept.  

-   Biome: <http://github.com/cjfields/biome>
-   BioPerl6: <http://github.com/cjfields/bioperl6>

<!-- -->

-   IO implementations for object iteration, or Perl6 grammars for
    common formats
-   Redesign of common BioPerl classes
-   etc.

This is an area ripe for new student project ideas. The more focused the
better! Discussion is a must, either via IRC or email.

Difficulty : Project-dependent  

<!-- -->

Mentors : Chris Fields, Mark Jensen  

### Convert BioPerl-DB to DBIx::Class

Rationale : Bioperl-db (the BioPerl bindings to BioSQL) in essence constitute a self-made ORM, invented at a time when DBIx::Class didn't exist yet. As such, it has some advantages (if you are willing to count overly clever features to be counted in this category), but arguably many more disadvantages, chief among them being the unsustainably small (you could also say non-existent) developer community supporting it, and the fact that DBIx::Class now has existed for years, and is fairly mature. So, rewriting Bioperl-db with a DBIx::Class (or another well-supported generic ORM) would stand to make a considerable impact on our ability to further develop Bioperl's relational storage capabilities, as well as BioSQL itself.  

<!-- -->

Approach : Under the supervision of their mentor(s), the GSoC student will:  

:\* Start working on conversion of BioPerl-DB classes to using
DBIx::Class

:\* write additional tests and improve documentation as needed

Challenges : BioPerl-DB is self-contained; this may require looking at the BioSQL schema and determining whether there are specific areas that need the most focus.  

<!-- -->

Difficulty and needed skills : easy to hard, depending on student's familiarity with the tools to be used. Student will need:  

:\* excellent Perl programming skills, including familiarity with:

:\*\* DBIx::Class

Mentors : Hilmar Lapp, others?  

[BioJava](http://biojava.org/wiki/Google_Summer_of_Code)
--------------------------------------------------------

![](Biojava_logo_tiny.jpg "Biojava_logo_tiny.jpg")

-   [BioJava developer mailing
    list](http://lists.open-bio.org/mailman/listinfo/biojava-dev)
-   [BioJava modules](http://biojava.org/wiki/BioJava:Modules) as
    another source for student-conceived project ideas
-   Source code for [1](https://github.com/biojava/biojava/)

### Analysis methods for protein dynamics

Rationale  
Protein structures are dynamic entities, and understanding how proteins
move can be critical to understanding their function. BioJava has strong
support for representing static protein structures, but little support
for representing flexability and freedom of movement. Such methods would
enable users to better analyze enzymes, kinases, and other biological
molecules which are relevent to molecular biology and medicine.

<!-- -->

Approach  
Initial efforts will focus on implementing the [Gaussian Network
Model](http://en.wikipedia.org/wiki/Gaussian_network_model), a popular
method for normal mode analysis in proteins. The project will include
both an implementation of the algorithm and the development of tools for
visualizing protein motions.

<!-- -->

Languages and skill  
Candidate should be comfortable with Java. Familiarity with
bioinformatics and molecular dynamics would also be beneficial, although
this background information could be learned by a motivated student.

<!-- -->

Code  
BioJava source code is available at
[2](https://github.com/biojava/biojava/) (LGPL)

Visualization will use the [Jmol](http://jmol.sourceforge.net/)
molecular viewer (LGPL)

<!-- -->

Mentors  
???

[BioRuby](http://bioruby.open-bio.org/wiki/Google_Summer_of_Code)
-----------------------------------------------------------------

![](BioRuby_logo_tiny.png "BioRuby_logo_tiny.png")

-   [Developers mailing
    list](http://lists.open-bio.org/mailman/listinfo/bioruby)
-   [Source code](http://github.com/bioruby/bioruby/tree/master)
-   IRC: `#bioruby` on [Freenode](http://freenode.net)

### Add local realignment support to Sambamba

Rationale  
Sambamba is a multi-core alignment processor for next generation
sequencing

(BAM/SAM/CRAM formats). It mostly replaces the samtools software apart
from

the mpileup routine. To achieve that the local realignment routine of

samtools needs to be implemented in the D programming language,
preferably removing the bugs and

taking ideas from the freebayes local realignment implementation.

<!-- -->

Approach  
Implement a local realignment routine in D. Add mpileup support
to sambamaba.

Update the bioruby-samtools package to support sambamba.

<!-- -->

Languages and skill  
Able to read C code and willing to write high-performance software in D
(and some Ruby).

Basic understanding of probability theory

<!-- -->

Code  
Sambamba: <https://github.com/lomereiter/sambamba>

D language: <http://dlang.org/>

Bioruby-samtools gem: <http://biogems.info/>

<!-- -->

  
Notes on Samtools algorithms:
<https://www.broadinstitute.org/gatk/media/docs/Samtools.pdf>

Samtools indel caller code:
<https://github.com/samtools/samtools/blob/develop/bam2bcf_indel.c>

Samtools local realignment:
<https://github.com/samtools/samtools/blob/develop/kprobaln.c>

<!-- -->

Mentors  
Pjotr Prins, Artem Tarasov, Francesco Strozzi

### BLAST visualisation library for BioRuby and SequenceServer

Rationale  

It is now trivial to generate large amounts of DNA sequence data; the
challenge is making sense of such data. In many cases, researchers can
gain much from simple answers regarding small sets of previously
identified study sequences – for example determining whether the
sequences are present in a new dataset, or identifying the genetic
variation present in such sequences. BLAST is the most commonly used
tool for such analyses (&gt;100,000 citations; twice among the top 15
cited papers of all time). However it remains surprisingly challenging
to visualize BLAST results.

Approach  

-   The student will study existing BLAST visualization approaches
    including as part of:
    -   NCBI’s website
    -   SequenceServer
    -   dot-plot
    -   Kablammo <http://kablammo.wasmuthlab.org>
    -   Circos-type visualization
        <https://twitter.com/pjacock/statuses/484439588434636800>
    -   Genevalidator (a former GSoC project)
        <http://genevalidator.sbcs.qmul.ac.uk>
    -   and potentially others - BLAST overviews should be considered
        independently of visualization concerning individual hits.
-   Decide on architecture for implementing these (or a subset) on
    Sequenceserver
-   Integrate visualization as part of sequenceserver - in a manner that
    further improves Sequenceserver’s user experience.
-   Release the libraries in a modular and documented manner for reuse
    by others.
-   This will require use of at least the following technologies: Ruby,
    Javascript, HTML, CSS.

Languages and skill  

Ruby, JavaScript

Code  

<https://github.com/yannickwurm/sequenceserver>
<https://github.com/jwintersinger/kablammo>

Mentors  

Yannick Wurm, Anurag Priyam

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

Rationale  
Fast k-mer indexing requires a data structure mapping a short string of
k characters to a value. While trivial to do with almost all key-value
maps, we also require a very memory-efficient storage system. Knowledge
of suffix structures is a definite plus.

<!-- -->

Approach  
Determine feasibility of implementation in pure Haskell vs. binding to
new or existing C code. Multi-threadedness will pose a problem. There is
currently no efficient suffix tree implementation available in Haskell
(lazy suffix trees do exist but are efficient only under
certain conditions).

<!-- -->

Languages and skill  
Haskell, maybe C (low-level code). Skill: need to have worked with
suffix structures before GSoC starts. If in coded in C, then enough
Haskell knowledge to be able to create thread-safe bindings. Otherwise,
medium to advanced Haskell knowledge.

<!-- -->

Code  
[containers](http://hackage.haskell.org/package/containers) and
[unordered
containers](http://hackage.haskell.org/package/unordered-containers) for
references to map-like container structures.

<!-- -->

Mentors  
Ketil Malde

### Low-level bit and stream-fusion optimizations

Rationale  
In Haskell, we typically don't talk that much about low-level
implementation details. For some algorithms, low-level details
(especially bitwise operations and SIMD instructions) become important.
I have a library dealing with bitsets but it is not yet fully efficient.
Getting SIMD instructions to play nice with /generic/ dynamic
programming recursion schemes is probably really hard.

<!-- -->

Approach  
Write benchmarking code for the different bit-manipulating functions.
Optimize the code to be as loopless as possible. Allow for
architecture-dependend code rewrites. The SIMD question is rather
open-ended and could very well be a Haskell.org task.

<!-- -->

Languages and skill  
Haskell and C. Bitset operations require knowledge of specialized
C routines. Including IFDef-ing for different architectures. Code should
be as non-branching / non-recursive as possible. SIMD instructions have
been added to vector library. The problem we face is that vector-SIMD
code expects data to be ordered linearly. Dynamic programming code leads
to unordered access structures. The student should know about the Core
language (one of the intermediate languages between Haskell and the
final binary).

<!-- -->

Code  
[vector](http://hackage.haskell.org/package/vector) for streaming code.
[bits](http://hackage.haskell.org/package/bits) for some
bitwise operations. An Ordered-Bits library will be pushed to hackage
next week with reference code. Dynamic programming code requires
[primitive arrays](http://hackage.haskell.org/package/PrimitiveArray)
and [ADPfusion](http://hackage.haskell.org/package/ADPfusion).

<!-- -->

Mentors  
Christian Hoener zu Siederdissen

[Team YummyData](https://github.com/dbcls/bh14/wiki/Yummydata)
--------------------------------------------------------------

YummyData is a system of collecting and disseminating various
statistical and functional data of SARQL endpoints in the Life Science
domain.

### Sharing SPARQL endpoint data

Rationale  
Although increasing amounts of biomedical data is being provided as
Linked Data, there is currently no standardized way to monitor SPARQL
endpoints for their availability, reliability, or content flux.

Importantly, there are additional issues relating to the provision of
version-sensitive data republished by third parties or made available as
part of research projects.

All of these aspects have important consequences for users that rely on
federated queries across distributed SPARQL endpoints.

<!-- -->

Approach  
YummyData system consists of mainly two components: that of collecting
data for each endpoint and that of providing obtained data.

Those data to be collected are based on variety of factors including
availability, reliability, content summarization, and content evolution.

Our long term goal is to compute a SPARKLE score, a composite metric
combining measures such as the number of triples, size and frequency of
updates, the number of links to other datasets, and the capabilities of
the endpoint server.

<!-- -->

Languages and skill  
YummyData system is written Java and Scala. In addition, SPARQL is used
to collect data, and JavaScript is used for showing results.

<!-- -->

Code  
[GitHub](https://github.com/sgtp/yummydata)

<!-- -->

Mentors  
Andrea Splendiani, Thierry Lombardot, Yasunori Yamamoto


