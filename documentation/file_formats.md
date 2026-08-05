Complex Portal provides its data in 3 different file formats, PSI-MI XML, MI-JSON and ComplexTab. Below are links to our schemas and some content explanations. For details on curation strategies, please see the [Data Content](/complexportal/documentation) section. All files can be downloaded from the Downloads section of the homepage and from our [ftp site](https://ftp.ebi.ac.uk/pub/databases/intact/complex/current/), and will be updated as we add new complexes with every data release.

## PSI-MI XML

### Schema

The schema and full details are found [here](https://www.psidev.info/mif)

## MI-JSON

### Schema

The schema and full details are found [here](https://github.com/MICommunity/psi-jami/tree/master/jami-interactionviewer-json)

### Notes

The MI-JSON provides the core interaction data, including all binding features, in a more concise format than PSI-MI XML for use cases where the XML files are too large to transfer in a reasonable amount of time. It removes the following content:

- annotations, such as function and properties description, complex assembly, disease statements

- component cross-references, while it retains the interaction (=complex) cross-references

- component aliases, such as gene names, secondary UniProt IDs

Use case: [ComplexViewer](https://github.com/MICommunity/ComplexViewer)

## ComplexTab

### Column definitions

1. Complex ac: unique, primary identifier for a complex represented as “CPX-{0-9}”. This column should never be empty ('-').

2. Recommended name: Most common name the complex is known by in the community. This column should never be empty ('-').

3. Aliases for complex: Synonyms. Multiple identifiers are separated by "|".

4. Taxonomy identifier: NCBI taxonomy identifier (id), represented as integer {0-9}. For host-pathogen complexes this is the pathogen id. This column should never be empty ('-').

5. Identifiers (and stoichiometry) of molecules in complex: represented as "ac(stoichiometry)”. For proteins the accession (ac) is UniProtKB, for chemical entities ChEBI, for RNA RNAcentral and for complexes Complex Portal. When the stoichiometry of a molecule is unknown, it is represented by (0). This column should never be empty ('-'). Multiple identifiers are separated by "|".

6. Confidence: represented by "ac(name)" where ac is the primary accession of the entry in the Evidence & Conclusion Ontology and name the term name. This column should never be empty ('-').

7. Experimental evidence: represented as “databaseName:ac” where databaseName is the name of an IMEx member database, wwPDB or EMDB as defined in the  PSI-MI controlled vocabulary and ac is the primary accession of an entry in that database that holds experimental evidence for the complex. This column is required if column 6 has codes ECO:0000353 or ECO:0005543 and should have a single value.

8. GO Annotations: Gene Ontology (GO) annotation of the complex represented as "ac(name)" where ac is the primary accession of the entry and name the term name in the GO database. Multiple annotations are separated by "|".

9. Cross references: represented as “databaseName:ac(qualifier)”, where databaseName is the name of the corresponding database as defined in the PSI-MI controlled vocabulary, the ac is the primary accession of the entry in the database and the qualifier the type of cross reference. Multiple annotations are separated by "|".

10. Description: free-text annotation topic "curated-complex". Describes the complex and its function. This column should never be empty ('-').

11. Complex properties: free-text annotation corresponding "complex-properties". Describes further information about the complex. Optional.

12. Complex assembly: free-text annotation topic "complex-assembly". Optional. This column should have a single value.

13. Ligand: free-text annotation topic "Ligand". Optional. Multiple annotations are separated by "|".

14. Disease: free-text annotation topic "Disease". Optional. Multiple annotations are separated by "|".

15. Agonist: free-text annotation topic "Agonist". Optional. Multiple annotations are separated by "|".

16. Antagonist: free-text annotation topic "Antagonist". Optional. Multiple annotations are separated by "|".

17. Comment: free-text annotation topic "Comment". Optional. Multiple annotations are separated by "|".

18. Source: database associated with the curator of the complex, represented as “psi-mi:”ac”(sourceName)” where ac is the primary accession and sourceName the name of the source database as defined in the PSI-MI controlled vocabulary. This column should never be empty ('-').

19. Expanded component list: lists only UniProt ac’s and stoichiometry from column 5 represented as "ac(stoichiometry)”, where UniProt ac’s are expanded for components that are complexes. This column should never be empty ('-'). Multiple identifiers are separated by "|".
