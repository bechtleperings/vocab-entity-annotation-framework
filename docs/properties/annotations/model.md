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