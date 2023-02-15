# Layers in the knowledge graph

This framework builds on the assumption that we can separate a knowledge graph in the following distinctive layers: 

### Layer 1: Entities
the immutable entities layer (or data, or documents, or whatever): the baseline, storing the facts. The facts are either stored only in the graph, or are shadow copies from a remote third-party application through connectors. Standard reasoning and business rules is used to alter the state of this layer.

### Layer 2: Assertions

Represents the modifiable part of the knowledge graph. 

Can be relations which link different entities on the entity layer. 

Can also be new properties (also overwriting existing properties on the entities layer)

Does also include annotations (e.g. tags, keywords, comments). 


### Layer 3: Recommendations

The recommendation layer consists of statements about statements. 

These are suggestions to augment and enrich the assertion layer

assertions about edges and values. The assertions are either coming from user feedback or from ML models.




### How do the relate (according to ChatGPT)?
Facts, assertions, and recommendations are all concepts that relate to knowledge and decision-making.

Facts are pieces of information that are objectively true and verifiable. They are typically established through research, observation, or other forms of evidence-based inquiry. Examples of facts might include demographic data, historical events, or scientific principles. 

Assertions, on the other hand, are claims or statements that are made about a particular situation or set of circumstances. Assertions can be based on facts, but they can also be subjective or opinion-based. For example, an assertion might be made about the effectiveness of a particular marketing strategy or the potential impact of a new policy proposal.

Recommendations are similar to assertions, but they are typically focused on action or decision-making. Recommendations are suggestions or advice that are given to someone who is facing a particular challenge or problem. They are often based on a combination of facts and expert opinion, and are designed to help the recipient make a more informed and effective decision.

In the context of knowledge management, facts, assertions, and recommendations can all be used to support decision-making and improve organizational performance. Facts can provide a foundation of objective information on which to base decisions, while assertions and recommendations can help to guide thinking and action in more subjective areas.

For example, in the context of data analysis, facts might include metrics such as sales figures, customer demographics, or website traffic. Based on these facts, an analyst might make an assertion about which products are selling best or which customer segments are most profitable. Finally, a recommendation might be made about which marketing channels to invest in, based on the analyst's assertions and other relevant factors.

Overall, facts, assertions, and recommendations are all important components of effective decision-making and knowledge management, and are often used in combination to support organizational goals and improve performance.