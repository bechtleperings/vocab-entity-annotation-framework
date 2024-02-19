---
hide:
  - toc
---

# Detail *updated*

The detailed parameter "updated" contains a timestamp in standard time format and is retained as a parameter during the generation of knowledge content by an LLM. It serves for time documentation to ensure the currency of knowledge. This facilitates the determination of outdated information to renew it.

### Schemata

````{.turtle hl_lines="14"}
@prefix rdf:    <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#> .
@prefix eav:    <http://w3id.org/eav/> . 

eav:updated a rdf:Property ;
  rdfs:label "updated" ;
  rdfs:comment  "DateTime string specifying the time of an update of the resource."@en ;
  rdfs:domain rdfs:Resource ;
  rdfs:isDefinedBy <http://www.w3id.org/eav> ;
  rdfs:range rdfs:Literal .
````