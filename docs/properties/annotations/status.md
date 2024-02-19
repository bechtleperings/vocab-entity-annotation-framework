---
hide:
  - toc
---

# Detail *status*

The detailed parameter "status" encompasses the current status of a piece of knowledge information. This includes storing information such as the availability or absence of a piece of information and its reason.

### Schemata

````{.turtle hl_lines="14"}
@prefix rdf:    <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#> .
@prefix eav:    <http://w3id.org/eav/> . 

eav:status a rdf:Property ;
  rdfs:label "status" ;
  rdfs:comment "String holding short and precise information about the actual status of the resource."@en ;
  rdfs:domain rdfs:Resource ;
  rdfs:isDefinedBy <http://www.w3id.org/eav> ;
  rdfs:range rdfs:Literal .

````