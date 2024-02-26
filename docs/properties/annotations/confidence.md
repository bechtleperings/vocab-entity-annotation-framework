---
hide:
  - toc
---

# Detail *confidence*

The detailed parameter "confidence" is queried during the generation of knowledge content by an LLM and describes the accuracy of the LLM in correctly answering the question. The LLM takes into account the amount of information received in order to provide a precise and likely correct response. The value is recorded as a decimal between 0 and 1, with anything below 0.6 to be approached with caution.

## Schemata

````turtle
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

## Example

```jsonld
"@context": {
  "hydra": http://www.w3.org/ns/hydra/core#,
  "sdo": https://schema.org/,
  "owl": http://www.w3.org/2002/07/owl#,
  "schema": http://schema.org/,
  "owl:sameAs": {
    "@id": "owl:sameAs",
    "@type": @id
    }
},
"@type": "schema:LearningResource",
"schema:name" : "Aufgabe aus \"Aufgaben zur Wahrscheinlichkeit\"",
"schema:audiences": {
  "@language": "en",
  "@value": "This learning resource, titled Aufgaben zur Wahrscheinlichkeit (Tasks on Probability), is likely intended for students studying mathematics, particularly those in upper secondary or tertiary education focusing on probability and statistics. The tasks may also be suitable for teachers or mentors preparing lessons on this topic, as well as trainees or professionals in fields requiring a good understanding of probability concepts.",
  "@annotation": {
    "eav:confidence": "0.85"
  }
}

```