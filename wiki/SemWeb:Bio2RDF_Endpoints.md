---
title: SemWeb:Bio2RDF Endpoints
---

Here are the current working Sparql Endpoints for Bio2RDF has of July
7th 2010, 16:37 PM

-   <http://pdb.bio2rdf.org/sparql>
-   <http://geneid-test.bio2rdf.org/sparql>
-   <http://pubmed.bio2rdf.org/sparql>
-   <http://refseq.bio2rdf.org/sparql>
-   <http://omim.bio2rdf.org/sparql>
-   <http://affymetrix.bio2rdf.org/sparql>
-   <http://atlas.bio2rdf.org/sparql>
-   <http://quebec.bio2rdf.org/sparql>
-   <http://bind.bio2rdf.org/sparql>
-   <http://biocarta.bio2rdf.org/sparql>
-   <http://biocyc.bio2rdf.org/sparql>
-   <http://biopax.bio2rdf.org/sparql>
-   <http://chebi.bio2rdf.org/sparql>
-   <http://cpath.bio2rdf.org/sparql>
-   <http://ec.bio2rdf.org/sparql>
-   <http://genbank.bio2rdf.org/sparql>
-   <http://geneid.bio2rdf.org/sparql>
-   <http://go.bio2rdf.org/sparql>
-   <http://hgnc.bio2rdf.org/sparql>

URI are build with this pattern

<http://bio2rdf.org/%5Bnamespace%5D>:\[identifier\]

To get information about this URI, you can either ask directly

<http://bio2rdf.org/%5Bnamespace%5D>:\[identifier\]

or ask the corresponding endpoint about it. The corresponding endpoints
is located at

<http://%5Bnamespace%5D.bio2rdf.org/sparql>

P.S.: The refseq endpoint is experimental. Instead of using the URI
pattern <http://bio2rdf.org/refseq>:\[identifier\] it use
<http://bio2rdf.org/ncbi>:\[identifier\]
