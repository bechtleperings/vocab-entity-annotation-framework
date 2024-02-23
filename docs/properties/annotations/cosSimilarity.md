---
hide:
  - toc
---

# Detail *cosSimilarity*

to be done...

## Schemata

```turtle
@prefix rdf:    <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#> .
@prefix eav:    <http://w3id.org/eav/> .

eav:cosSimilarity a rdf:Property;
  rdfs:label "cosSimilarity" ;
  rdfs:comment  "The cos similarity between the embeddings of the relevant descriptions / labels of the connected entities."@en ;
  rdfs:domain rdfs:Resource ;
  rdfs:isDefinedBy <http://www.w3id.org/eav> ;
  rdfs:range rdfs:Literal .  

```