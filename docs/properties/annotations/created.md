---
hide:
  - toc
---

# Detail *created*

The detailed parameter "created" contains a timestamp in standard time format and is retained as a parameter during the first generation of knowledge to specific content. Its purpose is time documentation.

### Schemata

````{.turtle hl_lines="14"}
@prefix rdf:    <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#> .
@prefix dct:    <http://purl.org/dc/terms#> .
@prefix owl:    <http://www.w3.org/2002/07/owl#> .
@prefix eav:    <http://w3id.org/eav/> . 

eav:created a rdf:Property ;
  owl:sameAs dct:created;
  rdfs:label "created" ;
  rdfs:comment "DateTime string specifying the time of creation of the resource."@en ;
  rdfs:domain rdfs:Resource ;
  rdfs:isDefinedBy <http://www.w3id.org/eav> ;
  rdfs:range rdfs:Literal .

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
      "schema:created": "2024-01-16T14:58:16.430601+00:00"
  }
}

```