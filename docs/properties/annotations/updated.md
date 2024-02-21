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
      "eav:updated": "2024-01-17T14:58:16.430601+00:00"
    ]
  ]

```