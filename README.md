# OntoME importer

This repository contains the script which transform an RDF ontology file into the format needed for its import into the [the Ontology Management Environment](https://ontome.net/), as well as small useful scripts to convert ontologies. Most scripts use the Python [rdflib library](https://github.com/RDFLib/rdflib) to import the ontology directly as a graph and write the output file directly from that graph.

## The scripts
The scripts included here may be executed via [Jupyter Notebook](https://jupyter.org/), if all the necessary Python libraries are installed (always see first code cell).
* [graph_to_ontome.ipynb](graph_to_ontome.ipynb) is the main script here, transforming a serialization into the OntoME import format. Any input format supported by RDFlib may be imported here.
* [import_crm.ipynb](import_crm.ipynb) is the state of the script before RDFlib was integrated and necessitates an RDFS-XML input file.
* [xml_to_dict.ipynb](xml_to_dict.ipynb) uses the Python xmltodict library, to output a Json file from any XML file.
* [ttl-to-rdfs.ipynb](ttl-to-rdf.ipynb) uses RDFlib to transform a Turtle format file into an XML-RDFs file.


## The folders
* [data](data) contains output files produced for punctual needs, possibly in a terminal without scripts. They are here merely for future reference.
* [input](input) contains only ontology description files which were given to, or are to be given to the main graph_to_ontome script.
* [output](output) contains the final significant results of the main graph_to_ontome script. Test output files made before the final state are not to be included in this public repository.
* [references](references) contains files useful to the main graph_to_ontome script, such as the XML schema for the output files and the dated Json representation of the namespaces already included in OntoME, along with their identifiers.
