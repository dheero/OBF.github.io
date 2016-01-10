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

<!-- -->

    select ?al ?o
    where {
    ?s a <http://bio2rdf.org/ns/affymetrix#Probeset> .
    ?s rdfs:label ?al .
    ?s ?p ?o .
    ?o bif:contains "calcium" .
    }
    limit 100

-   <http://atlas.bio2rdf.org/sparql> and \*
    <http://quebec.bio2rdf.org/sparql> are the same

<!-- -->

    SELECT ?label1, count(*)
    WHERE {
    ?s1 ?p1 ?o1 .
    ?s1 <http://www.w3.org/2000/01/rdf-schema#label> ?label1 .
    ?o1 bif:contains "morissette" .
    }
    ORDER BY DESC (count(*))

-   <http://bind.bio2rdf.org/sparql>

<!-- -->

    select ?inter ?inter2 ?part1_title ?part2_title ?part3_title 
    where {
    ?inter a <http://bio2rdf.org/bind#Interaction> .
    ?inter <http://bio2rdf.org/ns/ns/bind#interactionPart> ?part1 .
    ?inter <http://bio2rdf.org/ns/ns/bind#interactionPart> ?part2 .
    filter(?part1 != ?part2) .
    ?part1 <http://purl.org/dc/elements/1.1/title> ?part1_title .
    ?part2 <http://purl.org/dc/elements/1.1/title> ?part2_title .
    ?inter2 a <http://bio2rdf.org/bind#Interaction> .
    ?inter2 <http://bio2rdf.org/ns/ns/bind#interactionPart> ?part3 .
    ?inter2 <http://bio2rdf.org/ns/ns/bind#interactionPart> ?part4 .
    filter(?part3 != ?part4) .
    ?part3 <http://purl.org/dc/elements/1.1/title> ?part2_title .
    ?part4 <http://purl.org/dc/elements/1.1/title> ?part3_title .
    filter (?inter != ?inter2) .
    }
    limit 100

-   <http://biocarta.bio2rdf.org/sparql>
-   <http://biocyc.bio2rdf.org/sparql>

<!-- -->

    select distinct ?name ?LEFT_name ?RIGHT_name ?inter_name
    where {
    ?path a <http://bio2rdf.org/ns/biopax#pathway> .
    ?path <http://bio2rdf.org/ns/biopax#NAME> ?name .
    ?path <http://bio2rdf.org/ns/biopax#PATHWAY-COMPONENTS> ?comp .
    ?comp <http://bio2rdf.org/ns/biopax#STEP-INTERACTIONS> ?inter .
    ?inter <http://bio2rdf.org/ns/biopax#LEFT> ?LEFT .
    ?inter <http://bio2rdf.org/ns/biopax#RIGHT> ?RIGHT .
    ?inter <http://bio2rdf.org/ns/biopax#NAME> ?inter_name .
    ?LEFT ?p ?o .
    ?o <http://bio2rdf.org/ns/biopax#NAME> ?LEFT_name .
    ?RIGHT ?p2 ?o2 .
    ?o2 <http://bio2rdf.org/ns/biopax#NAME> ?RIGHT_name .
    }
    limit 100

-   <http://biopax.bio2rdf.org/sparql>

<!-- -->

    select ?name
    where {
    ?prot a <http://bio2rdf.org/ns/biopax#protein> .
    ?prot <http://bio2rdf.org/ns/biopax#SHORT-NAME> ?name .
    }
    limit 10

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
