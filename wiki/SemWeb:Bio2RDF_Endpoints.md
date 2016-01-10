---
title: SemWeb:Bio2RDF Endpoints
---

Here are the current working Sparql Endpoints for Bio2RDF has of July
7th 2010, 17:23 PM

-   <http://pdb.bio2rdf.org/sparql>

<!-- -->

    SELECT
    *
    WHERE
    {
    <http://bio2rdf.org/pdb:1GOF> ?p ?o .
    optional {?o ?p2 ?o2 .}
    optional {?o2 ?p3 ?o3 .}
    }

-   <http://geneid-test.bio2rdf.org/sparql>

<!-- -->

    select distinct ?g ?o
    where {
    graph ?g 
    {
    ?s ?p ?o .
    ?o bif:contains "HK1" .
    }
    }

-   <http://pubmed.bio2rdf.org/sparql>

<!-- -->

    select ?label ?o
    where
    {
    graph ?g {
    ?s ?p ?o .
    ?o bif:contains "HK1" .
    }
    graph ?g {
    ?s2 a <http://bio2rdf.org/pubmed:JournalArticle> .
    ?s2 rdfs:label ?label .
    }
    }
    limit 5

-   <http://refseq.bio2rdf.org/sparql>

<!-- -->

    select distinct ?rl ?fs ?fe
    where {
    ?o <http://bio2rdf.org/ncbi_resource:featureStart> ?fs .
    filter (xsd:integer(?fs) < 10000) 
    ?refseq <http://bio2rdf.org/ncbi_resource:feature> ?o .
    ?refseq rdfs:label $rl .
    ?o <http://bio2rdf.org/ncbi_resource:featureEnd> ?fe .
    }
    limit 5

-   <http://omim.bio2rdf.org/sparql>

<!-- -->

    select ?ol ?desc
    where {
    ?omim a <http://bio2rdf.org/omim_resource:MendelianDisorders> .
    ?omim rdfs:label ?ol .
    ?omim <http://purl.org/dc/terms/description> ?desc .
    ?desc bif:contains "HK1" .
    }
    limit 100

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
-   <http://homologene.bio2rdf.org/sparql>
-   <http://inoh.bio2rdf.org/sparql>
-   <http://iproclass.bio2rdf.org/sparql>
-   <http://kegg.bio2rdf.org/sparql>
-   <http://mesh.bio2rdf.org/sparql>
-   <http://mgi.bio2rdf.org/sparql>
-   <http://obo.bio2rdf.org/sparql>
-   <http://pid.bio2rdf.org/sparql>
-   <http://protein.bio2rdf.org/sparql>
-   <http://pubchem.bio2rdf.org/sparql>
-   <http://reactome.bio2rdf.org/sparql>
-   <http://registry.bio2rdf.org/sparql>
-   <http://release.bio2rdf.org/sparql>
-   <http://sgd.bio2rdf.org/sparql>
-   <http://taxonomy.bio2rdf.org/sparql>
-   <http://uniparc.bio2rdf.org/sparql>
-   <http://uniprot.bio2rdf.org/sparql>
-   <http://unists.bio2rdf.org/sparql>
-   <http://uniref.bio2rdf.org/sparql>

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
