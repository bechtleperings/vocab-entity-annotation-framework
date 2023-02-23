---
hide:
  - toc
---


# Property *acknowledgeCount*


A recommendation has been acknowledged, if a user is following the suggestion in the application. 

## Schema

````ttl
@prefix rdf:    <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd:    <http://www.w3.org/2001/XMLSchema#> .
@prefix eaf:    <http://w3id.org/eaf> . 
@prefix sdo:    <https://schema.org/> .


eaf:acknowledgeCount a rdfs:Property
    rdfs:label "count of acknowledgements"@en ;
    rdfs:comment "Implicit user feedback counting the number of interactions, where a user followed a recommendation"@en ;
    vann:usageNote "(statement) eaf:acknowledgeCount (predicate) xsd:integer (object)"@en ;

````


## Example

````ttl
@prefix : <http://example.org/>
@prefix sdo: <https://schema.org/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .
@prefix skill: <http://data.europa.eu/esco/skill> .
@prefix esco: <http://data.europa.eu/esco/> .
@prefix rec: <http://purl.org/ontology/rec/core#> .


:x a sdo:LearningResource
   sdo:title "Brew your own beer. Leaction 5: Roasting the malt."
   sdo:teaches esco:871c3f9f-c5ba-41bc-8978-71ef940c149d

<<:x sdo:teaches esco:871c3f9f-c5ba-41bc-8978-71ef940c149d>> a sdo:Recommendation
    eaf:confidence "0.7"
    eaf:acknowledgeCount 23

````