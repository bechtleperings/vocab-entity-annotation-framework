---
hide:
  - toc
---

# Detail *model*

The detailed parameter "model" returns, as a string, the model of the LLM used as the basis for generating the displayed information. If this parameter is not set, it defaults to the [standard defined LLM](../explanation.md#llm-usage).

### Schemata

````{.turtle hl_lines="14"}
@prefix rdf:    <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#> .
@prefix eav:    <http://w3id.org/eav/> . 

eav:model a rdf:Property ;
  rdfs:label "model" ;
  rdfs:comment "String holding short and precise information about the method of creation of the resource."@en ;
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
      "schema:model": "TheBloke/Mistral-7B-Instruct-v0.2-GGUF/mistral-7b-instruct-v0.2.Q5_K_M.gguf"
  }
}

```