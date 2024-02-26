---
hide:
  - toc
---

# Detail *cosSimilarity*

Describes the similarity of the give information with the pre defined standard information. This works based on their vector similarity in 600 dimensional arrays. More infromation in [this wiki](https://en.wikipedia.org/wiki/Cosine_similarity).

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
    "https://w3id.org/eav/cosSimilarity": " "
  }
}
```