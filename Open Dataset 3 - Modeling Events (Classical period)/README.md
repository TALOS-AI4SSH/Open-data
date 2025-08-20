# LACRIMALit Ontology (v1.0)

Maria Papadopoulou<sup>1,\*</sup>, Christophe Roche<sup>2</sup>  

*<sup>1</sup> Department of Philology, University of Crete, Greece<br/>
<sup>2</sup> TALOS ERA Chair Professor, University of Crete, Greece<br/>
<sup>\*</sup> Correspondence: [maria.papadopoulou@uoc.gr](mailto:maria.papadopoulou@uoc.gr)*  

Contributions and feedback are highly encouraged.  
Please send suggestions to **[maria.papadopoulou@uoc.gr](mailto:maria.papadopoulou@uoc.gr)**.

---

**Version 1.0 of the LACRIMALit Ontology**: an event-centric ontology designed to model **political crises in ancient history**.

Developed within the TALOS AI4SSH project, it provides formal representations of crisis events and their semantic relations, enabling structured exploration of ancient historiography.  

---

[![Download Ontology](https://img.shields.io/badge/Ontology-OWL%20Download-green.svg)](http://ontologia.fr/OTB/lac.owl)  
[![WebVOWL](https://img.shields.io/badge/Visualize-WebVOWL-blue.svg)](https://service.tib.eu/webvowl/#iri=http://ontologia.fr/OTB/lac.owl)  
[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-nd/4.0/)

---

## Software Environment
This ontology was created and managed with [Protégé](https://protege.stanford.edu/) (open access ontology editor).  

---

## Query the LACRIMALit Ontology

- **SPARQL Endpoint 1 (TALOS Dashboard):** [Open](http://147.52.205.216:8080/TALOSdashboard/)  
- **SPARQL Endpoint 2 (SPARQLer):** [Open SPARQLer](http://sparql.org/sparql.html)  

### Example query (CQ1)
*What are the different types of political crises?*
```sparql
# CQ1: What are the different types of political crises?
PREFIX rdf:  <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX owl:  <http://www.w3.org/2002/07/owl#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd:  <http://www.w3.org/2001/XMLSchema#>
PREFIX skos: <http://www.w3.org/2004/02/skos/core#>
PREFIX foaf: <http://xmlns.com/foaf/0.1/>
PREFIX lac:  <http://ontologia.fr/OTB/lac#>

SELECT DISTINCT ?crisisName
FROM <http://ontologia.fr/OTB/lac.owl>
WHERE {
  ?crisis rdfs:subClassOf* lac:Political_Crisis .
  ?crisis rdfs:label ?crisisName
}
ORDER BY ?crisisName 
```

[![SPARQL Queries (GitHub)](https://img.shields.io/badge/SPARQL-GitHub-black.svg)](https://github.com/MariaPapadopoulou/CBench/blob/master/sparql_lacrimalit_1.ipynb)  
[![Colab](https://img.shields.io/badge/SPARQL-Google%20Colab-orange.svg)](https://colab.research.google.com/github/MariaPapadopoulou/CBench/blob/master/sparql_lacrimalit_1.ipynb)

---

## Publications

- Papadopoulou, M., Roche, C., & Tamiolaki, E.-M. (2022).  
  *The LACRIMALit Ontology of Crisis: An Event-Centric Model for Digital History*.  
  **Information, 13**(8), 398.  
  [https://doi.org/10.3390/info13080398](https://www.mdpi.com/2078-2489/13/8/398)

- Papadopoulou, M., Tamiolaki, E.-M., & Roche, C. (2021).  
  *Crisis in troubled ancient times: ontological modeling of textual evidence from Greek historians*.  
  In **TOTh 2021: Terminology & Ontology – Theories and Applications**, Chambéry, France, 3–4 June 2021.  
  [Conference](http://toth.condillac.org/wp-content/uploads/2021/04/TOTh_2021_Final_Program_Online_En.pdf)

  ---

## Additional Resources

- **LACRIMALit portal** (O4DH): [o4dh.com/lacrimalit](http://o4dh.com/lacrimalit) — Access documentation, supplementary materials, and exploration interfaces.