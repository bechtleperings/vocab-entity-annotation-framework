# Entity Annotation Framework

A knowledge graph is typically described as a network of entities and there relationships. A common definition does not exist [^1]. It is typically associated with Semantic Web Technologies such as RDF or OWL. The Knowledge Graph places no limits on the kind of knowledge captured in its nodes and edges. Sensor data, abstract concepts, .. anything goes as long as it can be expressed in properties and relations. The proposed annotation framework is limited to individual entities (or just "individuals"). An entity has an identity, typically expressed through a name (aka named entities such as place names or persons) or globally unique identifiers (or "characteristic properties" [^2])

The proposed framework provides a common vocabulary to capture recommendations and annotations for entities, typically coming from users, statistical models and/or machine-learning models. While the entity graph captures knowledge about our world, the annotations capture our assumptions about certain properties of these entities.

Further information about: 

* [Annotations](definitions/Annotations.md)
* [Recommendations](definitions/Recommendations.md.md)



[^1]: EHRLINGER, Lisa; WÖß, Wolfram. [Towards a definition of knowledge graphs](https://ceur-ws.org/Vol-1695/paper4.pdf). SEMANTiCS (Posters, Demos, SuCCESS), 2016, 48. Jg., Nr. 1-4, S. 2. 
[^2]: GUARINO, Nicola; WELTY, Christopher. [A formal ontology of properties](https://link.springer.com/book/10.1007/3-540-39967-4#page=110). In: Knowledge Engineering and Knowledge Management Methods, Models, and Tools: 12th International Conference, EKAW 2000 Juan-les-Pins, France, October 2–6, 2000 Proceedings 12. Springer Berlin Heidelberg, 2000. S. 97-112.