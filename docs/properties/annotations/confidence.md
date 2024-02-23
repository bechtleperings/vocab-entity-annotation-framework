---
hide:
  - toc
---

# Detail *confidence*

The detailed parameter "confidence" is queried during the generation of knowledge content by an LLM and describes the accuracy of the LLM in correctly answering the question. The LLM takes into account the amount of information received in order to provide a precise and likely correct response. The value is recorded as a decimal between 0 and 1, with anything below 0.6 to be approached with caution.

## Schemata

````turtle
@prefix rdf:    <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd:    <http://www.w3.org/2001/XMLSchema#> .
@prefix eav:    <http://w3id.org/eav/> . 

eav:confidence a rdf:Property ;
  rdfs:label "confidence" ;
  rdfs:comment "Numerical value as a measure of trust into the statement."@en ;
  rdfs:domain rdfs:Resource ;
  rdfs:isDefinedBy <http://www.w3id.org/eav> ;
  rdfs:range xsd:float .
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
  sdo:name : "Aufgabe aus \"Aufgaben zur Wahrscheinlichkeit\""
  sdo:audiences: [
    "@language": "en",
    "@value": "This learning resource, titled Aufgaben zur Wahrscheinlichkeit (Tasks on Probability), is likely intended for students studying mathematics, particularly those in upper secondary or tertiary education focusing on probability and statistics. The tasks may also be suitable for teachers or mentors preparing lessons on this topic, as well as trainees or professionals in fields requiring a good understanding of probability concepts.",
    "@annotation": [
      "eav:confidence": "0.85"
    ]
  ]

```










<head>
  <!-- Prism.js library -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.24.1/themes/prism.min.css">
  <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.24.1/prism.min.js"></script>

  <!-- Prism.js line numbering plugin -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.24.1/plugins/line-numbers/prism-line-numbers.min.css">
  <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.24.1/plugins/line-numbers/prism-line-numbers.min.js"></script>

  <!-- Prism.js language support for JSON -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.24.1/components/prism-json.min.js"></script>
  
  <!-- Prism.js language support for Turtle -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.24.1/components/prism-turtle.min.js"></script>
  
  <style>
    .line-numbers .line-numbers-rows {
      pointer-events: none;
    }
  </style>
</head>




<div id="code-toggle" style="margin-bottom: 10px;">
  <button id="jsonld-button" onclick="showJsonLD()" style="padding: 5px 10px; background-color: #f0f0f0; border: 1px solid #ccc; cursor: pointer;">JSON-LD</button>
  <button id="turtle-button" onclick="showTurtle()" style="padding: 5px 10px; background-color: #f0f0f0; border: 1px solid #ccc; cursor: pointer;">Turtle</button>
</div>

<pre id="code-block" class="line-numbers">
  <code id="jsonld-code" class="language-json">
{
  "@context": "http://schema.org/",
  "@type": "Person",
  "name": "John Doe",
  "jobTitle": "Software Engineer",
  "memberOf": {
    "@type": "Organization",
    "name": "ABC Company"
  }
}
  </code>
  <code id="turtle-code" class="language-turtle" style="display: none;">
@prefix schema: <http://schema.org/> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix foaf: <http://xmlns.com/foaf/0.1/> .
@prefix ex: <http://example.com/> .

ex:JohnDoe a schema:Person ;
  foaf:name "John Doe" ;
  schema:jobTitle "Software Engineer" ;
  schema:memberOf [
    a schema:Organization ;
    schema:name "ABC Company"
  ] .
  </code>
</pre>

<script>
  Prism.highlightAll();
</script>


<script>
  function showJsonLD() {
    document.getElementById("jsonld-button").style.backgroundColor = "#4CAF50";
    document.getElementById("turtle-button").style.backgroundColor = "#f0f0f0";
    document.getElementById("jsonld-code").style.display = "block";
    document.getElementById("turtle-code").style.display = "none";
  }

  function showTurtle() {
    document.getElementById("turtle-button").style.backgroundColor = "#4CAF50";
    document.getElementById("jsonld-button").style.backgroundColor = "#f0f0f0";
    document.getElementById("turtle-code").style.display = "block";
    document.getElementById("jsonld-code").style.display = "none";
  }
</script>
