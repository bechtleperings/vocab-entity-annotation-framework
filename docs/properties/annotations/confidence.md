---
hide:
  - toc
---

# Detail *confidence*

## Schemata

````{.turtle hl_lines="14"}
@prefix rdf:    <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd:    <http://www.w3.org/2001/XMLSchema#> .
@prefix eav:    <http://w3id.org/eav/> . 

eav:confidence a rdf:Property ;
  rdfs:label "confidence" ;
  rdfs:comment "Numerical value as a measure of trust into the statement."@en ;
  rdfs:domain rdfs:Resource ;
  rdfs:isDefinedBy <http://www.w3id.org/eav> ;
  rdfs:range xsd:float .
````