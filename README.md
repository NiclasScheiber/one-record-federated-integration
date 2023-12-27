# one-record-federated-integration
Sample integration ontology of the ONE Record datamodel and the FEDeRATED semantic model. It includes a test dataset and a sample SPARQL query.

URIs are non-resolvable as the ontology is just for demonstration purpose. It integrates the models in the following ontologies:
ONE Record cargo ontology: 3.0.0
FEDeRATED Event ontology: 2020-07-17
FEDeRATED Digital Twin ontology: 2020-07-17
FEDeRATED Business Service ontology: 2020-07-20
FEDeRATED Physical Infrastructure ontology: 2020-07-17

## Covered concepts

The ontology covers the following concepts:

| FEDeRATED concept               | ONE Record 3.0 concept                                                                                                            |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ArrivalEvent	                  | MovementTimes & TransportMovement with direction=INBOUND                                                                          |
| DepartureEvent	          | MovementTimes & TransportMovement with direction=OUTBOUND                                                                         |
| DischargeEvent	          | Loading & TransportMovement with loadingType=UNLOADING                                                                            |
| LoadEvent	                  | Loading & TransportMovement with loadingType=LOADING                                                                              |
| StripEvent	                  | Composing & UnitComposition with compositionType=COMPOSITION                                                                      |
| StuffEvent	                  | Composing & UnitComposition with compositionType=DECOMPOSITION                                                                    |
| Goods                           | Piece                                                                                                                             |
| ULD	                          | ULD                                                                                                                               |
| Airplane	                  | TransportMeans                                                                                                                    |
| Location	                  | Location                                                                                                                          |

## Test data

This repository contains ONE Record test data (4.000 LogisticsObjects) to try the SPARQL query. 

The test data was randomly generated as part of the Digital Avatar sub-project of research project Digitales Testfeld Air Cargo (DTAC), sponsored by the German Ministry for Digital and Transport.

## Usage

Load the test data into a graph database that supports reasoning. Be sure to select an OWL-2.0 ruleset for reasoning. Apply the SPARQL query.