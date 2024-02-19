---
hide:
  - toc
---
# Property structure

The "Details" in the entitygraph are meant to contain information about the "Values" in the form of RDF* annotations to the corresponding "quoted triple" 

``<< <entity-urn> <property> value >>``

The Details are therefore of the form

``quoted_triple <detail_property> detail_value``


<br/>
<br/>

# Datenraum

## All steps to process the data from *Datenraum* - the central data pool for the [Bildungsraum](https://www.meinbildungsraum.de) project:

### 1. Loading nodes from *Datenraum* into the entity graph

The structure of the nodes may be inferred by the example in
[pull-updates-from-datenraum](https://dev.azure.com/av360/Artificial%20-%20The%20Intelligents/_git/scripts_e365.pipelines?path=/dags/datenraum)

The proposed Detail for the entities created from the Datenraum nodes is
> `eav:status "new"`

### 2. Application of Machine Learning models on the data

Models generate new content e.g. abstracts, keywords, target groups, transcriptions, etc. from the data.

The way of data generation is a complex process which can therefore only give a suggestion for a feasible content for the given aspect, so that we propose the following Detail value:

> `eav:status "suggested"`

### 3. Automated selection process of resulting content by given criteria

Using model confidence values to select the AI-generated content of sufficient quality to be feed back as proposal to the Datenraum.

The discussion at the Weekly rejected the proposed Detail value "validated" for this step to be too strong, as a real validation is a much more specific and detailed examination of the validity of the resulting content for the given subject. 

So the following Detail is suggested to be used here:
> `eav:status "approved"`

### 4. Proposing new metadata as *edges* for Datenraum

In the final step the resulting content is feed back to Datenraum as proposal for new edges. As this means a publication of our results to Datenraum we set the Detail of the corresponding statements in the entitygraph to: 
> `eav:status "published"`

# LLM usage

Our default LLM is ...