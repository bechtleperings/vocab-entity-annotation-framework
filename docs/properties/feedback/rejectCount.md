# Rejected recommendations

Rejecting a recommendation is a explicit feedback. A user may choose to ignore a recommendation due to unknown reasons, many of those might be irrelevant for improving the recommandations. Rejecting a recommendation, on the other hand, means a user has invested time and effort to explicitly state, that this particular suggestion is in now way meaningful in the current context. 

A rejection may be accompanied with explicit user feedback. 

Rejection and confirmation can be combined, asking a user with a "thumbs up" or "thumbs down" feedback. 



## Schema

````turtle
@prefix rdf:    <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd:    <http://www.w3.org/2001/XMLSchema#> .
@prefix eaf:    <http://w3id.org/eaf> . 
@prefix sdo:    <https://schema.org/> .


eaf:rejectCount a rdfs:Property
    rdfs:label "rejected recommendations count"@en ;
    rdfs:comment "Explicit user feedback counting the number of interactions, where a user rejected a recommendation"@en ;
    vann:usageNote "<statement> (subject) eaf:rejectCount (predicate) xsd:integer (object)"@en ;

eaf:rejection a rdfs:Property
    rdfs:label "details for rejected recommendation"@en ;
    rdfs:comment "Explicit user feedback giving details for a rejection"@en ;
    vann:usageNote "<statement> (subject) eaf:rejection (predicate) eaf:UserFeedback (object)"@en ;

eaf:UserFeedback a rdfs:Class
    rdfs:label "details for explicit feedback"@en ;


````