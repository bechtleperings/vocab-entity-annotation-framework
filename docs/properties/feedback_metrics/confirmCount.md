---
hide:
  - toc
---


# Explicit confirmation of a recommendation


## Schema
````{.turtle title="Schema"}
@prefix rdf:    <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd:    <http://www.w3.org/2001/XMLSchema#> .
@prefix eav:    <http://w3id.org/eav> . 
@prefix sdo:    <https://schema.org/> .


eav:confirmCount a rdfs:Property
    rdfs:label "confirmed recommendations count"@en ;
    rdfs:comment "Explicit user feedback counting the number of interactions, where a user confirmed a recommendation"@en ;
    vann:usageNote "<statement> (subject) eav:confirmCount (predicate) xsd:integer (object)"@en ;

eav:positiveFeedback a rdfs:Property
    rdfs:label "a user comment with positive feedback"@en ;
    rdfs:comment "Explicit user feedback giving details for agreement"@en ;
    vann:usageNote "<statement> (subject) eav:positiveFeedback (predicate) "comment" (object)"@en ;

````


A user can confirm a recommendation. 

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
  sdo:title "Brew your own beer. Leaction 5: Roasting the malt."
  sdo:teaches esco:871c3f9f-c5ba-41bc-8978-71ef940c149d

<<:x sdo:teaches esco:871c3f9f-c5ba-41bc-8978-71ef940c149d>>
  a eav:Recommendation
  eav:confirmCount 42
  eav:rejectCount  12
  eav:positiveFeedback "good recommendation"

```