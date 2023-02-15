# Maverick Annotation Framework
A knowledge graph is typically described as a network of entities and there relationships. A common definition does not exist [1]. It is typically associated with Semantic Web Technologies such as RDF or OWL. The Knowledge Graph places no limits on the kind of knowledge captured in its nodes and edges. Sensor data, abstract concepts, .. anything goes as long as it can be expressed in properties and relations. The proposed annotation framework is limited to individual entities (or just "individuals"). An entity has an identity, typically expressed through a name (aka named entities such as place names or persons) or globally unique identifiers (or "characteristic properties" [2])

The proposed framework provides a common vocabulary to capture recommendations and annotations for entities, typically coming from users, statistical models and/or machine-learning models. While the entity graph captures knowledge about our world, the annotations capture our assumptions about certain properties of these entities.


## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
