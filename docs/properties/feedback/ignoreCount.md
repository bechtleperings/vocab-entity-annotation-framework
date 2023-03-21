---
hide:
  - toc
---

# Ignored recommendations


There can be several reasons for ignoring a recommendation, including:

* Lack of trust: The recipient may not trust the source of the recommendation, the methodology used to generate it, or the accuracy of the data on which it is based.
* Limited resources: The recipient may not have the time, money, or other resources necessary to implement the recommendation, or may have other higher-priority initiatives to focus on.
* Conflicting priorities: The recipient may have different goals or priorities than those reflected in the recommendation, making it difficult to justify following it.
* Insufficient information: The recommendation may not provide enough context or detail to fully understand its implications, making it difficult to evaluate its relevance or feasibility.
* Organizational culture: The recipient's organization may have cultural or structural barriers that make it difficult to implement the recommendation, such as a lack of support from management or resistance to change.
* Personal biases: The recipient may have personal biases or preferences that conflict with the recommendation, such as a preference for certain vendors or approaches.
* Unforeseen circumstances: The recommendation may become irrelevant due to unforeseen circumstances, such as a change in market conditions or a shift in the political or regulatory landscape.

In some cases, ignoring a recommendation may be appropriate if the recipient has carefully evaluated it and determined that it is not in the organization's best interests to follow it. However, it is important to carefully consider the reasons for ignoring a recommendation, and to document the decision-making process to ensure transparency and accountability.

## Schema

````turtle
@prefix rdf:    <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd:    <http://www.w3.org/2001/XMLSchema#> .
@prefix eaf:    <http://w3id.org/eaf> . 
@prefix sdo:    <https://schema.org/> .


eaf:ignoreCount a rdfs:Property
    rdfs:label "ignored recommendations count"@en ;
    rdfs:comment "Implicit user feedback counting the number of interactions, where a user ignored a recommendation"@en ;
    vann:usageNote "(statement) eaf:acknowledgeCount (predicate) xsd:integer (object)"@en ;

````


## Example

````turtle
@prefix eaf: <http://w3id.org/avs/eaf>
@prefix sdo: <https://schema.org/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .
@prefix skill: <http://data.europa.eu/esco/skill> .
@prefix esco: <http://data.europa.eu/esco/> .
@prefix rec: <http://purl.org/ontology/rec/core#> .


:x a sdo:LearningResource
   sdo:title "Brew your own beer. Leaction 5: Roasting the malt."
   sdo:teaches esco:871c3f9f-c5ba-41bc-8978-71ef940c149d

<<:x sdo:teaches esco:871c3f9f-c5ba-41bc-8978-71ef940c149d>>
    eaf:confidence "0.2"
    eaf:ignoreCount 54
    eaf:acknowledgeCount 12

````


## Notes

### Distinctions

In relation to the [[rejectCount.md]], ignoring a recommendation is implicit (no active feedback by the user is required)

### Measuring

It can be a bit tricky to measure if a user is ignoring a recommendation. It can have multiple reasons: 

* the user doesn't follow the recommendation (reasons stated above). In this case we are interested in the feedback. 
* the user abandoned the overall topic, e.g. because of distractions, time issues, etc. 
* any kind of technical interruption
* a second recommendation seems to be more relevant