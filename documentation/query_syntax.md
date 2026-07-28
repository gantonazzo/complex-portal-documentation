## Complex Query

To do a search you can use the Complex Query Language (CQL), which is based on Lucene's syntax.

Free text search will look by default for:
- Identifiers, names and synonyms of molecules (protein, gene, small molecule)
- Identifiers, names and synonyms of complexes
- Cross-references of complexes
- Species
- Search for groups of complexes by using the Gene Ontology. For example, GO:0016491 will search for all complexes annotated with "oxidoreductase activity" and all downstream child terms of this.

Narrow your initial search result by using the filters on the results page for:
- Species
- Molecule type
- Biological role

## Complex Query Language (CQL) fields

|Field Name            | Searches on                                                          | Example  |
|----------------------|----------------------------------------------------------------------|----------|
|`complex_id`          | Complex identifier(s)                                                |[complex_id:CPX-2158](https://www.ebi.ac.uk/complexportal/complex/search?query=complex_id:CPX-2158 "Search by complex ac")|
|`complex_alias`       | Complex alias(es)                                                    |[complex_alias:"coenzyme Q-cytochrome c reductase"](https://www.ebi.ac.uk/complexportal/complex/search?query=complex_alias:&quot;coenzyme+Q-cytochrome+c+reductase&quot;)|
|`species`             | Complex Tax ID                                                       |[species:9606](https://www.ebi.ac.uk/complexportal/complex/search?query=species:9606)|
|`complex_xref`        | Complex xref(s)                                                      |[complex_xref:15210332](https://www.ebi.ac.uk/complexportal/complex/search?query=complex_xref:15210332)|
|`udate`               | Last update of the interaction                                       |[udate:\[20110607 TO 20120906\]](https://www.ebi.ac.uk/complexportal/complex/search?query=udate:[20110607+TO+20120906])|
|`id`                  | Component identifier(s)                                              |[id:P38326](https://www.ebi.ac.uk/complexportal/complex/search?query=id:P38326)|
|`alias`               | Component alias(es)                                                  |[alias:Cyclin](https://www.ebi.ac.uk/complexportal/complex/search?query=alias:Cyclin)|
|`ptype`               | Component type(s)                                                    |[ptype:protein](https://www.ebi.ac.uk/complexportal/complex/search?query=ptype:protein)|
|`pxref`               | Component xref(s)                                                    |[pxref:GO:0031577](https://www.ebi.ac.uk/complexportal/complex/search?query=pxref:GO:0031577)|
|`stc`                 | Boolean value to know if the Component has stoichiometry information |[stc:true](https://www.ebi.ac.uk/complexportal/complex/search?query=stc:true)|
|`pbiorole`            | Biological role(s)                                                   |[pbiorole:enzyme](https://www.ebi.ac.uk/complexportal/complex/search?query=pbiorole:enzyme)|
|`ftype`               | Feature type(s)                                                      |[ftype:"binding region"](https://www.ebi.ac.uk/complexportal/complex/search?query=ftype:&quot;binding+region&quot;)|
|`source`              | Source database(s)                                                   |[source:intact](https://www.ebi.ac.uk/complexportal/complex/search?query=source:intact)|
|`number_participants` | Number of components                                                 |[number_participants:3](https://www.ebi.ac.uk/complexportal/complex/search?query=number_participants:3)|

