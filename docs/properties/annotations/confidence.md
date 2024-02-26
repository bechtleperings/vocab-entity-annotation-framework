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

```turtle
@prefix : <http://example.org/>
@prefix sdo: <https://schema.org/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .
@prefix skill: <http://data.europa.eu/esco/skill> .
@prefix esco: <http://data.europa.eu/esco/> .
@prefix rec: <http://purl.org/ontology/rec/core#> .
@prefix eav: <http://w3id.org/eav/> . 


:x a sdo:LearningResource
  sdo:name : "Aufgabe aus \"Aufgaben zur Wahrscheinlichkeit\""
  sdo:audiences: [
    "@language": "en",
    "@value": "This learning resource, titled Aufgaben zur Wahrscheinlichkeit (Tasks on Probability), is likely intended for students studying mathematics, particularly those in upper secondary or tertiary education focusing on probability and statistics. The tasks may also be suitable for teachers or mentors preparing lessons on this topic, as well as trainees or professionals in fields requiring a good understanding of probability concepts.",
    "@annotation": [
      "eav:confidence": "0.85"
    ]
  ]

```