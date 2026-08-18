---
onenote-id: 0-492f5934e872431d9f857d5e805b0775!1-D084F068F621FF9!3928
---
XML
 
- Simple
- Flexible
- Can have attributes on tags
- Must be "well-formed"
- Define schema or DTD
	- DTD has different syntax
   

- Tags are _domain-terms_
	- Don't provide semantics to machines
- Define structure
	- Not the meaning of the contents
- Lacks a semantic model
	- Only a _surface model_
 
- Only for closed collaboration
- Small & stable community
- Not for heterogeneous devices
	- Not for web-resources

Resource Description Framework  
RDF
 
- W3C recommendation
- Relationships between documents
- \<subject, property, object\>
	- \<“Sensor”, hasType, “Temperature”\>
- RDFS
	- Extension with _ontology vocabulary_
- Can be written in XML
- Form a graph
 ![has Time Data 815 hasZone Time hasSecond Zone Hour...](../../../../../img/OneNote/Semantics%20image%20b1ff83f4107e8463.png)  

- Object -\> Attribute -\> Value
- Object -\> Property -\> Subject
 
- Resource
	- Each has URI
	- Can be used as URL
- Property
	- Special kind of resources
	- Relations between resources
	- Also identified by URI
	- SPARQL
		- Query language for RDF

![Machine generated alternative text hasTime xsdtime...](../../../../../img/OneNote/Semantics%20image%20267ab438819d5896.png)  
![Machine generated alternative text 0815 hasLongitu...](../../../../../img/OneNote/Semantics%20image%20bf343fed9502f512.png)  
![Machine generated alternative text rdf RDF rdf Des...](../../../../../img/OneNote/Semantics%20image%204ff051c4e5dbe83f.png)

![Machine generated alternative text xsd time hasT i...](../../../../../img/OneNote/Semantics%20image%204112720ba1ffa54a.png)

Ontologies
 
- _Study of the nature of existence_
- Extension of semantic technologies
- Formal specification of a domain
	- Concepts in a domain
	- Relationships between concepts
		- Logical restrictions
- Classes & properties
	- Schema ontology
- Engineering
	1. Define classes and arrange into taxonomy
	2. Define properties and allowed values
	3. Add instances and individuals
- No one correct way to model
	- Often iterative
 
# Web Ontology Language

OWL

- Describe ontologies
- Supports
	- Equality
	- Property characteristics
	- Property restrictions
	- Restricted cardinality
	- Class intersection
	- Annotation properties
	- Versioning

1. Determine domain & scope
2. See which concepts/ontologies can be reused
3. Enumerate important terms
	- Will identify key classes
4. Define classes and hierarchy
5. Define class properties and relationships
6. Define features of properties
	1. Restrictions/logical expressions
7. Define/add instances

JSON
 
# JSON-LD

- Serialise linked data
	- RDF data connected to other resources

![httpmyonot10gyschemeSensorName Vleee , httpmyonotI...](../../../../../img/OneNote/Semantics%20image%204be1a4d6ca0e7541.png)

- Context
	- Work in a shared environment

![EXAMPLE 3 Context for the sample document in the p...](../../../../../img/OneNote/Semantics%20image%202dc746f025652e16.png)

Semantics
 
- Interoperability
- Effective data access & integration
- Resource discovery
- Processing of data
- Information extraction

**Lightweight**  
**Compatibility**  
**Modularity**

![only Deployme ntRelatedPrccesS Deployment d only i...](../../../../../img/OneNote/Semantics%20image%20232804d67750e3f7.png)

Web of Things
 
_Integrating the real world data into the Web and providing Web-based interactions with the IoT resources_
 
- Large in scale, volume
- Continuous
	- Spatiotemporal dependency

