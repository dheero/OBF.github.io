---
title: BOSC 2007 Abstracts
---

BOSC 2007 Abstracts
===================

\[New Technology\] The Galaxy Framework for Computational Biology Tool Integration
----------------------------------------------------------------------------------

James Taylor, Visiting Member, Courant Institute, New York University

Modern biology is being revolutionized by high throughput data
production, and an amazing number of powerful tools for analyzing
biological data have been developed. However a substantial challenge
remains: how to provide these tools in an integrated environment that is
accessible not just to software developers, but to experimental
biologists. We have developed a system -- Galaxy -- to address this
challenge. Galaxy provides a framework that allows existing
computational tools to easily be given modern web based interfaces, and
integrated with other computational tools to facilitate complex
multi-stage analysis. Galaxy simultaneously targets two audiences: for
tool developers it eliminates the repetitive effort involved in creating
high-quality user interfaces, while giving them the benefit of being
able to provide their tools in an integrated environment. For
experimental biologist it allows running complex analysis on huge
datasets without needing to worry about details of installing tools,
allocating computing resources, and file format conversions. This talk
will discuss the Galaxy architecture, how it can help computational tool
developers, the advantages of tool integration, and future directions.

\[New Technology\] AJAX GBrowse: Community Genome Annotation Made Easy
----------------------------------------------------------------------

Mitch Skinner, Berkeley University

The current standard for genome browser software involves a user
interface based on static web pages. These pages are created on a server
from a pre-loaded database of genome features, then viewed re-motely on
a web browser. It is desirable to improve on this general approach by
adding two new kinds of feature:

1.  Instant responsiveness. In current browsers, whenever the user
    requests an action (such as moving to a new genome location, zooming
    in/out, changing view properties, etc.) the server must perform
    various database and page-rendering operations. This causes a
    significant lag, even if only a small part of the view is changed.
2.  Persistent community annotation. In a typical system, entry of new
    annotations is dependent on a database administrator. While some
    genome browsers allow user-generated annotations to be tran-siently
    displayed alongside 'official' tracks, there is typically no
    mechanism for permanently entering new records over the web. This
    has the potential to slow down community annotation.

While somewhat independent, both of these features are typical of a new
generation of Web 2.0 applications. We have extended the GBrowse
open-source genome browser to implement these ideas, using the
recently-popularized AJAX (Asynchronous Java Script And XML) framework,
whereby a carefully designated proportion of the computational load is
shifted from the database server to the web-browsing client. The new
framework enables a much smoother interface, familiar to users of
websites such as Google Maps. For example, chromosome views can be
dynamically dragged in a continuous motion without noticeable delay.
Similarly, tracks can be instantly collapsed or expanded, with no
waiting time while the new view is downloaded over the network. Our
approach also empowers true community annotation, whereby users can add
their own tracks to a genome browser for others to see, constituting a
'live genome wiki'. We currently support feature uploads in GFF format,
and we will soon support the WIG format as well. We intend to provide
our browser to the modENCODE project. We are currently porting all
existing GBrowse functionality to this new system. As a demonstration we
have working browsers for D.melanogaster and S.cerevisiae chromosomes
viewable at <http://genome.biowiki.org/>.

-   License: Artistic
-   Web site: <http://genome.biowiki.org>
-   Email: gmod-ajax@lists.sourceforge.net

\[New Technology\] Dasty2: A Web Client for Visualizing Protein Sequence Features
---------------------------------------------------------------------------------

Rafael C. Jimenez, European Bioinformatics Institute, Hinxton, Cambridge

We present Dasty2 (1), a web client for visualizing protein sequence
feature information using the Distributed Annotation System (DAS) (2,3).
The client establishes connections to a DAS reference server to retrieve
sequence information and to one or more DAS annotation servers to
retrieve feature annotations (4). It merges the collected data from all
these servers and provides the user with a unified, aesthetically
pleasing, effective view of the sequence-annotated features. Dasty2 uses
AJAX to deliver highly interactive graphical functionality in a web
browser by executing multiple asynchronous DAS requests. Dasty2 has two
main modules, retrieval and visualization, as shown in Figure 1. The
retrieval module works on the server side. It retrieves annotations from
DAS servers and makes them available to the visualization module. The
visualization module resides on the client side and facilitates the
visualization of the information obtained from the retrieval module. The
retrieval module is a CGI program written in Perl. It can be ported to
other programming languages to ease integration into other web
applications. The retrieval module is used by Dasty2 but can also be
used independently to retrieve XML files from different sources. The CGI
program can be executed in any web browser by specifying query
parameters in the URL field. It can retrieve feature and stylesheet
files from annotation servers, sequence files from reference servers as
well as a list of available DAS servers from the DAS registry (5). The
visualization module is based on AJAX. It incorporates standards-based
presentation using HTML and Cascading Style Sheets (CSS), dynamic
display and interaction using the Document Object Model (DOM),
asynchronous data retrieval using the XMLHttpRequest class and
JavaScript binding everything together.

The visualization module allows asynchronous loading of information so
that protein feature annotations can be displayed as soon as annotation
from the first DAS server is provided. Once the information has been
retrieved by the client, it is cached, eliminating the need for further
server requests for most visual manipulations, such as sorting by
feature. The asynchronous loading and local caching of results enabled
by using AJAX improve usability and system response time (6).
Technically, Dasty2 is web-browser compatible, lightweight, independent
from third party software, easy to integrate into other web based
systems, efficient when loading and manipulating annotations, highly
configurable and customizable, and interactive and intuitive for users.
By being web-based, it is more readily accessible to biological
researchers, as they do not need to install specialized software to run
it (7). Being JavaScript-based, it is easy for developers to integrate
it into their own web systems. Customizability aids this. The use of
AJAX improves efficiency when displaying information. Finally, because
of its independence from large, complicated third-party libraries and
its modularity, Dasty2 is easy to extend.

Visually, Dasty2 provides numerous advantages over other DAS clients
(8). Space is used effectively so there is no need to scroll in portions
of the screen. It makes use of the standard colours employed by Uniprot
and SRS for annotations. Dasty2 uses colours, borders, complimentary
shades and separating lines to contrast features with the background and
to make the relationships among annotations clear (9). Finally, Dasty2
allows grouping and sorting of annotations by various properties, and
zooming within a protein sequence.

REFERENCES:

1.  Dasty, <http://www.ebi.ac.uk/dasty/>
2.  Dowell, R., Jokerst, R.M., Day, A., Eddy, S.R. & Stein, L. 2001. The
    Distributed Annotation. Sys-tem BMC Bioinformatics 2:7
3.  Biodas, <http://www.biodas.org>
4.  Jones, P., Vinod, N., Down, T., Hackmann, A., Kahari, A.,
    Kretschmann, E., Quinn, A., Wieser, D., Hermjakob, H. & Apweiler, R.
    2005. Dasty and UniProt DAS: a perfect pair for protein
    feature visu-alization. Bioinformatics, Oxford Univ Press 21,
    3198-3199
5.  DAS registry, <http://www.dasregistry.org>
6.  Paulson, L. 2005. Building rich web applications with Ajax. Computer
    38, 14-17

-   OPEN SOURCE LICENSE All Dasty2 software is freely available to all
    users, academic or commercial, under the terms of the Apache License
    Version 2.0
-   PROJECT WEBSITE <http://www.ebi.ac.uk/dasty/>
-   CONTACT EMAIL List: dasty-help@ebi.ac.uk Personal: rafael@ebi.ac.uk

\[New Technology\] EMBRACE Web Services
---------------------------------------

Taavi Hupponen, CSC, the Finnish IT center for science

One of the main goals of the EU FP6 -funded EMBRACE
(http://www.embracegrid.info) is to enable programmatic remote access to
bioinformatics tools and databases through standard interfaces. As
opposed to traditional web-based interfaces, this will allow the
services to be accessed efficiently from own software or from tools like
the workflow-enactment engine Taverna (http://taverna.sourceforge.net/).

The technology of choice for providing the service interfaces is SOAP
based Web services. As interoperability is essential for successful
integration, the use of specifications and best practices such as the
WS-I Basic Profile and document literal wrapped style have been
emphasized in interface implementations. Also issues like managing state
and dealing with large data have received attention. EMBRACE Web
services are listed at <http://www.embracegrid.info/dokuwiki/> and they
include for example tools for sequence and structure analysis as well as
several bioinformatics databases.

EMBRACE is funded by the European Commission within its FP6 Programme,
under the thematic area "Life sciences, genomics and biotechnology for
health,"contract number LHSG-CT-2004-512092.

-   Web site: <http://www.embracegrid.info>
-   Contact: Taavi Hupponen, CSC, Finland, taavi.hupponen@csc.fi

\[New Technology\] CaGrid Cancer Biomedical Informatics Grid
------------------------------------------------------------

Krishnakant Shanbhag, NCI Center for Bioinformatics

The goal of cancer Biomedical Informatics Grid caBIG(tm) is to develop
applications and the underlying systems architecture that connects
together data, tools, scientists and organizations in an open federated
environment. In meeting this goal, caBIG will necessarily bring together
data from many and diverse data sources. The underlying service oriented
infrastructure for caBIG is caGrid. caGrid defines two types of "grid
services" that can be registered as nodes on the grid: Data Services and
Analytical Services. caGrid provides a standard infrastructure for
bioinformaticians to advertise their services thru common metadata
defined in Unified Modeling Language (UML) domain information model.
Users can access these grid services and data programmatically using
locally managed access control policies and using strongly typed data
objects in XML format. caGrid infrastructure also provides strong
semantic specification thru binding to description logic terminology
concepts that can be used by users to discover new and interesting
scientific information using semantically aware searches.

caGrid is built upon the relevant community-driven standards of the
World Wide Web Consortium (W3C ) <http://www.w3.org/> and OASIS
<http://www.oasis-open.org> . It is also informed by the efforts
underway in the Open Grid Forum (OGF) <http://ogf.org/> . As such, while
the caGrid infrastructure is built upon the 4.0 version of the Globus
Toolkit (GT4) <http://www.globus.org/toolkit/> , it shares a Globus
<http://www.globus.org/toolkit> goal to be programming language and
toolkit agnostic by leveraging existing standards. Specifically, caGrid
services are standard WSRF v1.2
<http://www.oasis-open.org/specs/index.php#wsrfv1.2> services and can be
accessed by any specification-compliant client. This presentation will
provide an overview of caGrid infrastructure and supporting tools that
are part of the project.

-   Project Web Site
    <https://cabig.nci.nih.gov/workspaces/Architecture/caGrid/>
-   Open Source License caGrid infrastructure uses a commercial friendly
    open source license.
-   License information:
    <http://ncicb.nci.nih.gov/download/cagridlicenseagreement.jsp>
-   Contact Information Email: shanbhak@mail.nih.gov

\[OS Software\] The ONDEX Data Integration Framework
----------------------------------------------------

Jan Taubert, Rothamsted Research

Systems Biology routinely requires the combined analysis of several
databases, text sources and experimental data. The open source framework
ONDEX provides technical and semantic integration and analysis for large
databases and free-text sources. Data integration and text mining in
ONDEX consists of 3 steps: 1) Databases are converted into a form
compliant with the unified ontology based data structure 2) Equivalent
and related entities in the heterogeneous data sources are identified 3)
Data analysis and knowledge extraction are applied to the integrated
data, which is a requirement for making sense of large integrated
datasets, composed of millions of linked elements ONDEX has several
important advantages over "traditional" data warehouses: a) An
application-independent database schema allows a large variety of
different data sources to be integrated without modifications to the
underlying schema. A traditional data warehouse would necessitate the
addition of new tables and fields as data sources invariably change b)
New data parsers can be developed independent of each other c) The
ontology/graph based data structure of ONDEX enabled us to combine
database integration methods with concept based text mining and graph
analysis.

ONDEX is 100% pure Java code and uses the Berkeley DB Java Edition and
Lucene. We provide Java interfaces and SOAP web services for querying
and analysing integrated data sets. In addition, web services exist
which allow the use of Taverna for configuring and running data
integration workflows. Currently supported databases include ARACYC,
DRASTIC, Enzyme Nomenclature, Gene Ontology, complete KEGG, complete
MEDLINE, Plant Ontology, TRANSFAC and TRANSPATH. Additional databases
can be easily added as plug-ins. Import parsers for PSI-MI, OBO, XGMML
and ONDEX XML exist. Currently data can be exported to the SBML, XGMML,
ONDEX XML, GML and GraphML formats. A graphical analysis front-end for
ONDEX provides visualisation and layout methods. Several data analysis
filters can be applied to support certain biological use case, e.g.
microarray analysis for integrated pathway data, combination of
transcriptomics and metabolomics analysis, and identification of highly
connected components in pathways.

The work on the ONDEX system was started in 2002. Since the last release
in 2005, the ONDEX system has been completely reengineered. The latest
developments can be retrieved from SourceForge

\[OS Software\] CGEMS: An Open-Source caIntegrator Application to support Whole Genome Association Studies
----------------------------------------------------------------------------------------------------------

Subhashree Madhavan, Ph.D., National Cancer Institute

Progress in finding better therapies for cancer treatment has been
hampered by the lack of opportunity to integrate biomedical data from
disparate sources to enable translation of critical information from
bench to bedside and back. Hence, a critical factor in the advancement
of biomedical research and delivery is the ease with which data can be
integrated, redistributed and analyzed both within and across functional
domains. The NCICB, in collaboration with NCI extramural and intramural
research groups, has developed a novel translational informatics
application called caIntegrator that allows physicians, researchers, and
bioinformaticians to access and analyze clinical and experimental data
across multiple clinical studies. We have leveraged the caIntegrator
application framework to build the CGEMS (Cancer Genetic Markers of
Susceptibility) data portal to support Whole Genome SNP association
studies.

Background on CGEMS: A Genome wide SNP association analysis has been
conducted in a large, national study in the U.S.A., the Prostate, Lung,
Colorectal, and Ovary study (PLCO). Phase 1 of the analysis includes
1,177 subjects who developed prostate cancer during the observational
period and 1,105 individuals who did not develop prostate cancer during
the same time period. The data generated from these scans can be
accessed through the CGEMS data portal
(https://caintegrator.nci.nih.gov/cgems/). The datasets available
through the portal include:

-   Association test results for over 300,000 SNPs
-   Frequency and descriptive statistics on these SNPs
-   Individual phenotypic and genotypic data for the study participants
    and control samples. Note that these data can only be made available
    to eligible investigators after a registration process.
-   Phase 2 of CGEMS includes data from GWAS (Genome wide
    association study) where 530000 SNPs were genotyped on breast
    samples from 1,145 cancer patients and 1,142 controls. The
    pre-computed SNP association results and population frequencies are
    made available via the CGEMS data portal.

caIntegrator technology: The heart of the caIntegrator framework is the
caBIG compliant Clinical Genomic Object Model (CGOM). Objects in CGOM
Study package represent the study, treatment arms, patient information,
histology, and information on the biospecimen. The 'Specimen Finding'
objects model the in-silico transformation and analyses performed on the
raw experimental datasets. The 'Clinical Finding' objects provide
clinical observations and assessments. 'Annotation' objects such as
GeneBiomarker, ProteinBiomarker and SNPAnnotation help to provide
context to various Findings. A new Findings package called
'GenotypeFinding' has been created in CGOM to support the CGEMS
datasets.

Following are high-level caIntegrator features used in the CGEMS data
portal development: A common set of interfaces (APIs) and specification
objects that define the clinical genomic analysis services. In other
words, they act as templates for the caIntegrator-based translational
application(s), which will extend and implement these interfaces and
specification objects. The application's user interface communicates
with its caIntegrator-based middle-tier services via domain as well as
business objects. The caIntegrator hybrid data system consists of a star
schema database which contains the clinical and annotation data as
dimensions, genotype, SNP association and SNP frequency data as facts,
and Common Security Model (CSM) tables for user provisioning data. This
caIntegrator translational framework offers a paradigm for rapid sharing
of information and accelerates the process of analyzing results from
various biomedical studies with the ultimate goal to rapidly change
routine patient care.

Resources:

-   CaIntegrator website: <http://caintegrator.nci.nih.gov>
-   CGEMS data portal: <http://caintegrator.nci.nih.gov/cgems>
-   CGEMS information site: <http://cgems.cancer.gov/>
-   CaIntegrator open source license:
    <http://ncicb.nci.nih.gov/download/caintegratorlicenseagreement.jsp>
-   CaIntegrator-WGS source code bundle and seed data:
    <http://gforge.nci.nih.gov/frs/?group_id=154>

\[OS Software\] Modware: An Object-Oriented Perl Interface to the Chado Schema
------------------------------------------------------------------------------

Eric Just, Center for Genetic Medicine, Feinberg School of Medicine,
Nortwestern University, Chicago, IL

Chado was developed as a relational database schema for storing genomic
data for FlyBase. Subsequently, Chado was adopted and distributed by the
Generic Model Organism Database (GMOD) Project and it is now in use by
numerous genome databases. Agile, dynamic applications that use Chado as
a data store require an intuitive application programming interface
(API) consisting of rich data objects that semantically resemble
biological entities. Such an API encourages faster development times by
encapsulating core logic while allowing developers to focus on new
challenges rather solving well-defined problems such as storage and
retrieval of common biological data structures. Modware is an
object-oriented Perl API developed to fill this need for bioinformatics
scientists and developers who use the Chado database. An object-oriented
API attempts to map data from relational tables to in-memory data
objects. Augmenting the often-used one-table/one-class method of
object-relational mapping, Modware collects data from many tables and
tuples into data structures that more closely resemble biological
entities. There are separate classes for chromosomes, mRNAs, and exons,
among others, but a parent class to handle common data and methods. In
addition, it provides a framework and methods to search, manipulate and
reformat this data. For sequence features, Modware directly uses
BioPerl's object-oriented interface which is already pervasive and
widely understood in the bioinformatics world. The object-relational
mapping layer based on Class::DBI and distributed by GMOD is used
internally to provide lower-level calls to the database. Performance is
optimized through the use of 'lazy evaluation'. Only when associated
data is requested is it retrieved from the database into memory. In
addition there are 'Search' classes which return groups of objects based
on search criteria. For instance, one can call a method to retrieve
genes which have names matching a wild card query or genes that fall in
a particular region on a chromosome. Modware was developed as middleware
for dictyBase but has been engineered to be organism and database
independent. It is open-source (BSD License) and has been carefully
documented on the web along with the source code and quick-start guide
at:

-   <http://gmod-ware.sourceforge.net>.
-   Open Source License: BSD
-   Project website: <http://gmod-ware.sourceforge.net>

\[OS Software\] XRATE: Scheme-y trees, phylo-HMMs and phylo-grammars
--------------------------------------------------------------------

Ian Holmes, Berkeley University

A big hit in the past couple of years has been the "phylo-HMM", a
multi-sequence HMM employing Felsenstein's pruning algorithm to compute
emission scores. (Stochastic grammar extensions to this idea include
phylo-GHMMs and phylo-SCFGs.) The phylo-HMM idea was first introduced
for genome analysis by Churchill and Felsenstein, and further developed
e.g. for RNA structure prediction by Knudsen and Hein. The use of
phylo-grammars by Siepel, Pedersen, Bejerano, Haussler et al for gene
prediction, evolutionary analysis of rate variation, and other forms of
genome annotation has gotten lots of attention in recent years.

Much of the appeal of phylo-grammars is the straight transfer of
intuition and expertise from the areas of HMMs and SCFGs. However, the
well-known EM algorithms used to train these models (Baum-Welch,
Inside-Outside) are a little less straightforward to apply to phylo-
grammars. In contrast to (say) Baum-Welch, the phylo-EM algorithm is
pretty hairy and not something you'd really want to implement twice. In
the past 4 years we have taken the theory of phylo-EM algorithms from a
theoretical treatment (Holmes & Rubin, JMB, 2002) up to a full- blown
open-source implementation of a general phylo-grammar prototyping,
training and annotation engine (XRATE). Grammars can be specified using
a Scheme-like format, "trained" on alignments using phylo-EM, and then
used to annotate alignments. The phylo-EM code in our open-source C++
library can also be linked to by external applications (e.g. Jakob
Pedersen's EVOFOLD program, which has been used to investigated
recently-evolving human ncRNAs). Several developers have contributed
full-time to the process, and there is considerable stability, including
a battery of automated tests.

XRATE is an easy-to-use Unix app that brings the unrestricted power of
phylo-grammars in reach of a first-year grad student or smart undergrad.
In a historical aside, XRATE has its roots in a grammar compiler,
TELEGRAPH, that was itself based on Ewan Birney's DYNAMITE (and is
related to Guy Slater's EXONERATE). TELEGRAPH was presented at BOSC
2000. At BOSC 2007, I'll show how far XRATE has come by giving a tour of
its rate-measurement and annotation abilities, accompanied by
visualizations of the interesting variety of patterns (covariation,
neighbor-dependence, conservation, lineage-specific acceleration,
selection...) that can be observed in the mutation rates of genomic
features.

Since the development of XRATE, a collection of phylo-grammars has begun
to accumulate from user contributions, along with various Perl and
Python scripting libraries for driving phylo-grammar development. I will
give a quick outline of these, and also describe how we are using XRATE
in production projects such as our (re)annotation pipeline for
Drosophila (and other "genome clades").

-   Project URL: <http://biowiki.org/dart>
-   License: GPL

\[OS Software\] E-Cell 3D: 3-Dimensional Visualization Front-End for E-Cell Simulation Environment
--------------------------------------------------------------------------------------------------

Kazuharu Arakawa, Institute for Advanced Biosciences, Keio University

Cell simulation realizes theoretical experiments in silico to enhance
our understanding of dynamic cellular activities through integrative
systems biology approaches. E-Cell Simulation Environment version 3
(E-Cell SE 3) is a potential platform for this purpose, which allows
object-oriented simulations with multiple algorithms and timescales.
However, simulation results that are typically shown in multiple graphs
representing the time-course progression of the changes in the
concentrations of cellular components is not scalable, and this approach
quickly becomes too intricate for human interpretations as the number of
components in the model increases.

Here we present a novel interface for this system using 3D graphics to
aid the understanding of highly complex systems by researchers in the
process of modeling through intuitive visualization. New interface
designated E-Cell 3D is developed with Quartz graphics API and OpenGL on
MacOS X, and visualizes the components and the reaction networks among
the components in 3-dimensional space. Components of the model stored in
Systems Biology Markup Language (SBML) XML file are automatically laid
out in 3-D space, and time- course progression of the components are
simulated using E-Cell SE 3, and are visualized through the E-Cell 3D
visualization engine. This visualization approach allows the user to
capture the entire system at a glance, and aids the heuristics of system
biologists in the process of modeling. The software and documentations
are freely available at <http://www.e-cell.org/>.

-   License: GPL
-   Website: <http://ecell3d.iab.keio.ac.jp/>
-   Contact E-mail: gaou@sfc.keio.ac.jp

\[OS Software\] XMLPipeDB: A Reusable, Open Source Tool Chain for Building Relational Databases from XML Sources
----------------------------------------------------------------------------------------------------------------

Kam Dahlquist, Department of Biology, Loyola Marymount University

XMLPipeDB is an open source suite of Java-based tools for automatically
building relational databases from an XML schema (XSD). XMLPipeDB
provides functionality for managing, querying, importing, and exporting
information to and from XML data with minimum manual processing of the
data. While its applicability is fairly general, the original motivation
for XMLPipeDB was to create a solution for the management of biological
data from different sources that are used to create Gene Databases for
GenMAPP (Gene Map Annotator and Pathway Profiler), software for viewing
and analyzing genomic-scale data on biological pathways. XMLPipeDB has
the following tools for developers and database designers: the XSD-to-DB
application takes a well-formed XSD or DTD file and converts it into a
collection of Java source code and Hibernate mapping files that allows
XML files based on that definition file to be read into a relational
database. XSD-to-DB's conversion functions are based on the open source
Hyperjaxb2 project, which adds Hibernate functionality to Sun
Microsystemsexpected by the GenMAPP application.

Last year at BOSC, we reported that we used the XMLPipeDB software tool
chain to create a relational databases for UniProt and Gene Ontology,
and that, in turn, we used these databases to generate UniProt-centric
GenMAPP Gene Databases for Escherichia coli K12. Although the production
of the E. coli K12 Gene Database was an important proof of concept,
several improvements were needed to make the system truly extensible to
other species. First, import of XML files larger than 50 MB caused the
software to crash because the JAXB unmarshaller was attempting to read
the entire file into memory before writing anything back to the
database. The import engine can now import files of any size because it
pre-processes the data into smaller blocks before passing them to the
unmarshaller. Second, unit tests and a tally engine that produces data
integrity reports were incorporated into the import and export process.
These features were added to the XMLPipeDB Utilities library and are
therefore available as part of a generic library. Third, GenMAPP Builder
was refactored to provide an export framework that was extensible to
other species, and the speed of the export was improved by about 20
percent. Finally, as a result of these improvements, we have created a
GenMAPP Gene Database for Arabidopsis thaliana.

-   License: GNU Library or Lesser General Public License (LGPL) at
-   Project Website: <http://xmlpipedb.cs.lmu.edu> or
    <http://sourceforge.net/projects/xmlpipedb>

\[Software Design And Engineering\] An Open Source Framework for Teaching Bioinformatics
----------------------------------------------------------------------------------------

Kam Dahlquist, Department of Biology, Loyola Marymount University

Bioinformatics training can be categorized into three areas: tool use,
algorithm design/theoretical foundations, and program development.
Courses emphasizing tool use are usually targeted at biologists, while
courses emphasizing algorithm design and theoretical foundations are
usually targeted at computer scientists. However, there are few (if any)
reports of courses that explicitly address how to teach the best
practices of software development for scientific computing. Pedagogical
practices in computer science itself are frequently disconnected from
the expectations and skill sets required of computer scientists in
industry or interdisciplinary research groups. Computer science
undergraduates typically work alone instead of in a team, produce
isolated programs from scratch instead of large modular projects, and
throw away their code after the assignment has been graded instead of
maintaining it over an extended period of time. Open source principles,
culture, and tools can be leveraged to teach best practices of software
development, including up-front project design, program and process
documentation, quality control, data standards, and project management.
Here we describe the implementation of an open source teaching framework
for bioinformatics that grew out of the Recourse computer science
curriculum development project at LMU (http://recourse.cs.lmu.edu/).

One mechanism by which the open source culture can be adapted to a
bioinformatics curriculum is to give students an authentic problem to
solve with software, one that is large enough to require a team effort.
XMLPipeDB (http://xmlpipedb.cs.lmu.edu/) is an open source suite of
Java-based tools for automatically building relational databases from an
XML schema (XSD). XMLPipeDB was developed by graduate students as part
of a team-taught course in bioinformatics that was then extended into a
second workshop course on open source software development. Throughout
this project, students were expected to uphold best practices of
software development. The students were asked to perform up-front
project design and program and process documentation. Quality control
came in the form of code reviews and bug tracking. The project itself
utilized XML data standards and was managed by the instructors with
cycles of design reviews, setting of milestones, and evaluation of
results. The students used open source tools throughout. Each student
chose their own development environment (e.g., Eclipse, NetBeans, text
editor + ant, etc.) but worked as a team from a SourceForge-hosted
repository. The added benefit of this open source teaching framework is
that it facilitates the long-term management of course projects beyond
the current semester and class. This framework enabled the students to
gain real world experience with open source software development and
proficiency with tools widely used by the open source community, while
making a concrete contribution to an open source software project.

\[Software Design And Engineering\] Tools to Facilitate Large Scale Comparative Genomic Analysis
------------------------------------------------------------------------------------------------

James Taylor, Visiting Member, Courant Institute, New York University

Performing almost any interesting analysis at the scale of multiple
genomes quickly becomes non-trivial. Analysis of this scale often
require a compromise between performance and clarity. Working with data
at this scale is even more challenging in research groups where storage
for large datasets (such as multi-species whole genome alignments) is a
shared resource accessed concurrently by many users. However, well
designed supporting tools can address many of these problems by wrapping
optimized algorithms in simple interfaces that allow rapid construction
of new analyses that are both high performance and easy to understand
and communicate.

The 'bx-python' packages is an open-source library and associated
command line tools designed to make large scale comparative genomic
analysis easy. It includes a library of reusable components focused on
simplifying highly repetitive yet performance critical tasks. For
example it includes support for

-   A generic data structure for indexing on disk files that contain
    blocks of data associated with inter-vals on various sequences
    (used, for example, to provide random access to individual
    alignments in huge files). The indexes are optimized for use over
    network filesystems, as well as reducing network overhead by
    providing random access to the indexed files
-   Support for indexing of and semi-random access to compressed files.
-   Components for reading and working with genome-scale multiple local
    alignments (in MAF, AXT, and LAV formats)
-   Data structures for working with intervals on sequences, including
    'binned bitsets' which act just like chromosome sized bit arrays,
    but lazily allocate regions and allow large blocks of all set or all
    unset bits to be stored compactly, without the user needing to worry
    about sequence size.

These components and the included command line tools are also a core
part of the Galaxy analysis platform (http://g2.bx.psu.edu), in
particular its support for genome scale interval operations and working
with alignments. Combined with Galaxy, 'bx-python' facilitates integrate
analysis by making it incredibly easy to develop tools for performing
large scale analysis efficiently, and making those tools available via
the web to data producers such as experimental biologists.

  
[ Back To BOSC 2007 Home](BOSC_2007 "wikilink")
