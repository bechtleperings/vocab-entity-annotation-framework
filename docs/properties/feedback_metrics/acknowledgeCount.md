---
hide:
  - toc
---

# Implicit acknowledgement of a recommendation. 


A recommendation has been acknowledged, if a user is following the suggestion in the application. 

When a recommendation is acknowledged, it means that the recipient has received and reviewed the recommendation, and has indicated their understanding and acceptance of it. Acknowledgement is an important step in the process of implementing recommendations, as it ensures that the recipient is aware of the recommendation and is prepared to take any necessary action.

Acknowledgement of a recommendation can take many forms, depending on the context and the relationship between the parties involved. In some cases, acknowledgement may simply involve an email or other form of communication confirming receipt of the recommendation. In other cases, it may involve a formal response indicating agreement or disagreement with the recommendation, and outlining any steps that will be taken in response.

In the context of knowledge management, acknowledgement of recommendations is an important part of the feedback loop that helps to refine and improve the knowledge base over time. By acknowledging recommendations and providing feedback on their effectiveness, users can help to ensure that the knowledge base remains relevant and valuable to the organization.

## Schema

````ttl
@prefix rdf:    <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd:    <http://www.w3.org/2001/XMLSchema#> .
@prefix eav:    <http://w3id.org/eav> . 
@prefix sdo:    <https://schema.org/> .


eav:acknowledgeCount a rdfs:Property
    rdfs:label "count of acknowledgements"@en ;
    rdfs:comment "Implicit user feedback counting the number of interactions, where a user followed a recommendation"@en ;
    vann:usageNote "(statement) eav:acknowledgeCount (predicate) xsd:integer (object)"@en ;

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
   sdo:title "Brew your own beer. Leaction 5: Roasting the malt."
   sdo:teaches esco:871c3f9f-c5ba-41bc-8978-71ef940c149d

<<:x sdo:teaches esco:871c3f9f-c5ba-41bc-8978-71ef940c149d>> 
    a eav:Recommendation
    eav:confidence "0.7"
    eav:acknowledgeCount 23

```

## Notes 

### InteractionCounter
Schema.org provides the [InteractionCounter](https://schema.org/InteractionCounter)

It would complicate the definition, and we cannot directly address the property details anymore. 

````
@prefix eav: <http://w3id.org/eav/> . 

eaf:AcknowledgeCounter rdfs:subClassOf sdo:InteractionCounter

:x a sdo:LearningResource
   sdo:title "Brew your own beer. Leaction 5: Roasting the malt."
   sdo:teaches esco:871c3f9f-c5ba-41bc-8978-71ef940c149d

<<:x sdo:teaches esco:871c3f9f-c5ba-41bc-8978-71ef940c149d>> a sdo:Recommendation
    eaf:confidence "0.7"
    sdo:interactionStatistic :y

y: a eaf:AcknowledgeCounter
   sdo:userInteractionCount 23
````