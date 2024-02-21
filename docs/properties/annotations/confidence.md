---
hide:
  - toc
---

# Detail *confidence*
![Bundesmin](/docs/assets/images/BMBF_Logo.jpg)
The detailed parameter "confidence" is queried during the generation of knowledge content by an LLM and describes the accuracy of the LLM in correctly answering the question. The LLM takes into account the amount of information received in order to provide a precise and likely correct response. The value is recorded as a decimal between 0 and 1, with anything below 0.6 to be approached with caution.

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