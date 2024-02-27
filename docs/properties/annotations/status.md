---
hide:
  - toc
---

# Detail *status*

The detailed parameter "status" encompasses the current status of a piece of knowledge information. This includes storing information such as the availability or absence of a piece of information and its reason. Possible statuses are: rejected, approved and suggested.

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
        "schema:status": "rejected"
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
      eav:status "rejected"
    ```