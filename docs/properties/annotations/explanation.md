---
hide:
  - toc
---

# Detail *explanation*

The detailed parameter "explanation" is queried during the generation of knowledge content by an LLM and describes the reasoning of the LLM why it chose this answer. The LLM describes their choice of confidence value by giving information about fulfilled criterias and incomplete input.

## Schemata

````{.turtle hl_lines="14"}
@prefix rdf:    <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd:    <http://www.w3.org/2001/XMLSchema#> .
@prefix eav:    <http://w3id.org/eav/> . 

eav:explanation a rdf:Property ;
  rdfs:label "confidence" ;
  rdfs:comment "Literal sentences explaining the choice of answer from llm."@en ;
  rdfs:domain rdfs:Resource ;
  rdfs:isDefinedBy <http://www.w3id.org/eav> ;
  rdfs:range xsd:float .
````

## Example

=== "jsonld"
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
        "schema:explanation": "The name Aufgaben zur Wahrscheinlichkeit suggests that the resource is related to probability learning, which is typically taught at advanced levels of mathematics education. The description does not indicate a specific audience beyond students and teachers, but given the nature of the content, it seems most likely to be targeted towards this demographic. However, it's also plausible that professionals or trainees in fields like finance, insurance, engineering, and data analysis might find value in using these tasks for self-study or review. The title and description do not suggest that the resource is intended for beginners, children, hobbyists, retirees, or the unemployed, although it could potentially be used as supplementary material for various audiences."
      }
    }
    ```

=== "turtle"
    ```turtle
    @prefix rdf:    <http://www.w3.org/1999/02/22-rdf-syntax-ns#> 
    @prefix sdo:    <https://schema.org/> .
    @prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#> .
    @prefix xsd:    <http://www.w3.org/2001/XMLSchema#> .
    @prefix eav:    <http://w3id.org/eav/> . 

    :x a sdo:LearningResource
      sdo:name "Aufgabe aus \"Aufgaben zur Wahrscheinlichkeit\""
      sdo:audiences "This learning resource, titled Aufgaben zur Wahrscheinlichkeit (Tasks on Probability), is  likely intended for students studying mathematics, particularly those in upper secondary or tertiary education focusing on probability and statistics. The tasks may also be suitable for teachers or mentors preparing lessons on this topic, as well as trainees or professionals in fields requiring a good understanding of probability concepts."
    
    <<:x sdo:audiences {...}>>
      eav:explanation "The name Aufgaben zur Wahrscheinlichkeit suggests that the resource is related to probability learning, which is typically taught at advanced levels of mathematics education. The description does not indicate a specific audience beyond students and teachers, but given the nature of the content, it seems most likely to be targeted towards this demographic. However, it's also plausible that professionals or trainees in fields like finance, insurance, engineering, and data analysis might find value in using these tasks for self-study or review. The title and description do not suggest that the resource is intended for beginners, children, hobbyists, retirees, or the unemployed, although it could potentially be used as supplementary material for various audiences."
    ```