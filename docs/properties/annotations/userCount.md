---
hide:
  - toc
---

# Property *userCount*

The number of users who have applied the annotation, eg. a keyword.

## Schema

````ttl
@prefix rdf:    <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd:    <http://www.w3.org/2001/XMLSchema#> .
@prefix eav:    <http://w3id.org/eav> . 
@prefix sdo:    <https://schema.org/> .


eav:userCount a rdfs:Property
    rdfs:label "count of users suggesting the annotation"@en ;
    rdfs:comment "Number of users who have applied the given annotation"@en ;

````


## Example

````ttl
@prefix : <http://example.org/>
@prefix sdo: <https://schema.org/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .
@prefix skill: <http://data.europa.eu/esco/skill> .
@prefix esco: <http://data.europa.eu/esco/> .
@prefix rec: <http://purl.org/ontology/rec/core#> .
@prefix eav: <http://w3id.org/eav/> . 


:x a sdo:LearningResource
   sdo:title "Brew your own beer. Leaction 5: Roasting the malt."
   sdo:keywords :y

:y a sdo:DefinedTerm
   sdo:value "diy"

<<:x sdo:keywords :y>> eav:userCount 2



````