## Data Content

### What is the Complex Portal?

The Complex Portal is a manually curated, encyclopedic resource of biologically functional and stable macromolecular complexes from a number of key model organisms. Complexes may contain proteins as well as small molecules and nucleic acids, providing they are an integral part of the complex.

In addition to the manually curated complexes, which adhere to this definition, the database provides extended coverage of the human complexome with high confidence assemblies of machine-learning predicted complexes.

### What can be described as a complex?

A stable set of (two or more) interacting macromolecules such as proteins which can be co-purified by an acceptable method and have been shown to exist as an isolated, functional unit in vivo. This definition has been extended to encompass molecules which associate to form scaffolding structures that are ready to recruit context-specific effector proteins to initiate activation of functionally distinct signalling pathways within the same physical multiprotein complexes. Any interacting, integral non-protein molecules (e.g. small molecules, nucleic acids) may also be included.

### What should **NOT** be captured:

- Enzyme/substrate, receptor/ligand or any similar transient interactions unless these are a critical part of the complex assembly (e.g. PDGF receptors only become 'dimeric' when linked by the dimeric ligand forming a tetramer).
- Proteins associated in a pulldown/coimmunoprecipitation with no functional link or any evidence that this is a defined biological entity rather than a loose affinity complex.
- Any literature complex where the only evidence is based on genetic interaction data.
- Partial complexes


### Tricky cases we **DO** capture:

- Substrates or ligands if the enzyme or receptor complex only forms in their presence (see PDGF receptors above, e.g. CPX-2883).
- Homologous proteins, with the same functionality, which would be inferred based on homology of the genome-encoded components made primarily on functional conservation between the two systems to form a complex but for which no physical link has been demonstrated, e.g. proteins A and B have been shown to physically interact and form a functional complex, protein C is a homologue of protein B by sequence similarity and is know to have the same function as B but protein A-C interaction has not been demonstrated experimentally (e.g. Deoxyribonuclease MUS81 complexes: there is interaction evidence for binding of MUS81 with EME1 ([CPX-511](https://www.ebi.ac.uk/complexportal/complex/CPX-511)) but not with EME2 ([CPX-586](https://www.ebi.ac.uk/complexportal/complex/CPX-586))). These complexes are tagged with [ECO:0005546 biological system reconstruction evidence based on paralogy evidence used in manual assertion](https://www.ebi.ac.uk/ols/ontologies/eco/terms?iri=http%3A%2F%2Fpurl.obolibrary.org%2Fobo%2FECO_0005546).
- Complexes which are generally assumed to exist but for which only partial experimental evidence exists (such as functional studies or ligand binding evidence from pharmacological experiments), e.g. [Muscle-type nicotinic acetylcholine receptor complex, alpha1-beta1-delta-gamma](https://www.ebi.ac.uk/complexportal/complex/CPX-2179). These complexes are tagged with [ECO:0005547 biological system reconstruction evidence based on inference from background scientific knowledge used in manual assertion](https://www.ebi.ac.uk/ols/ontologies/eco/terms?iri=http%3A%2F%2Fpurl.obolibrary.org%2Fobo%2FECO_0005547).

## Species

Currently, our curation focuses on model organisms and globally important micro-organisms.

### Multicellular organisms

We curate to species level (e.g. *[Homo sapiens](https://www.uniprot.org/taxonomy/9606)*, *[Mus musculus](https://www.uniprot.org/taxonomy/10090)*, *[Caenorhabditis elegans](https://www.uniprot.org/taxonomy/6239)*).  

### Micro-organisms

We curate to the model organism strain or reference proteome (e.g. [*Saccharomyces cerevisiae* (strain ATCC 204508 / S288c)](https://www.uniprot.org/taxonomy/559292), [*Escherichia coli* (strain K12)](https://www.uniprot.org/taxonomy/83333)).

In cases where an organism is not a model organisms but is of specific scientific interest we curate the complexes in the strain where the experimental evidence exists and, if possible, in the species level taxon (e.g. species [Human SARS coronavirus](https://www.uniprot.org/taxonomy/694009) and strain [Severe acute respiratory syndrome coronavirus 2](https://www.uniprot.org/taxonomy/2697049)). If the strain or species level taxon has multiple equal UniProt Trembl entries that cannot be distinguished we choose the strain that has experimental evidence or the reference proteome (e.g. for species [Middle East respiratory syndrome-related coronavirus](https://www.uniprot.org/taxonomy/1335626) only Trembl entries exist, while strain [Middle East respiratory syndrome-related coronavirus (isolate United Kingdom/H123990006/2012)](https://www.uniprot.org/taxonomy/1263720) is the reference proteome and several experiments also exist for strain [Middle East respiratory syndrome-related coronavirus (Human betacoronavirus 2c EMC/2012)](https://www.uniprot.org/taxonomy/1235996)).

### Host-pathogen complexes

At the moment, each complex can only be assigned one species. In order to be able to combine all complexes for a given pathogen the complex is assigned the pathogen species.

## Complex Nomenclature

### Complex recommended name

The most informative, well accepted name in the literature, that is intuitive to the user. Where possible, this will be the same as the equivalent component term in the [Gene Ontology](http://geneontology.org/). The term should always end in the word 'complex' or homo'n'mer. The recommended name is kept consistent when a complex is conserved across a taxonomic range. 

### Complex systematic name

This is a string of gene symbols of the complex components separated by a colon (e.g. "fiba:fibb:fibg") in alphanumeric order. The order is irrestective of species in a host-pathogen complex. Recommended gene symbols for each model organism will be used; therefore the systematic name may not be consistent when a complex is conserved across a taxonomic range. 

### Complex synonym

All other possible names the complex is known by or can be described as.

### Shortlabel (not displayed on website, only in download files)

An obligate part of the data model. An appropriate designation for the complex with species indicated using the UniProt five letter code e.g. fibrinogen_human, tfiid_mouse. When the same complex is conserved across a taxonomic range, the root name is maintained across all entries e.g. fibrinogen_human, fibrinogen_mouse, fibrinogen_bovin. 

The Shortlabel appears as "gene product name" when a Complex Portal AC is used as annotation object in Gene Ontology annotations.

## Complex Components

### Proteins

All proteins are derived from, and linked to, [UniProtKB](uniprot.org/) identifiers, ideally UniProtKB/Swiss-Prot. Isoform and chain designators are used when appropriate. Should one or more isoforms exist, annotation will be to the canonical protein entry unless either only one isoform is known to exist in the complex or different isoforms give the complex different properties. In the latter case, a separate entry should be made for each variation with detail given in the "Description" or "Properties" section as appropriate (see below for details on complex variants). 

### Small molecules / polysaccharides

All small molecules are derived from, and linked to, [ChEBI](https://www.ebi.ac.uk/chebi/) identifiers. Small molecules are included only if they are integral to the complex or bind to the complex as part of its function, e.g. cofactors, electron donors/acceptors, such as ATP, H+. Enzyme targets are not added as components. For example, ATP is entered as a cofactor if the enzyme function is NOT primarily an ATPase (e.g. [GyrA-GyrB DNA Gyrase complex](https://www.ebi.ac.uk/complexportal/complex/CPX-2177)) but NOT entered for ATPases where it is a substrate (e.g. [TRCF-UvrA complex](https://www.ebi.ac.uk/complexportal/complex/CPX-2155)). In the latter case the substrate is added using a [Gene Ontology](http://geneontology.org/) annotation, e.g. [ATP binding](https://www.ebi.ac.uk/QuickGO/term/GO:0005524).

### Nucleic acids

Nucleic acids are only entered as components when they are an obligate part of the complex. Non-coding RNA components are linked to [RNACentral](https://rnacentral.org/) identifiers, all other nucleic acid types are created as generic molecules linked to generic [ChEBI](https://www.ebi.ac.uk/chebi/) identifiers. For complexes which assemble and then bind to a nucleic acids, this function is indicated in free text and annotated using [Gene Ontology](http://geneontology.org/) terms such as [DNA binding](https://www.ebi.ac.uk/QuickGO/term/GO:0003677).

### Complexes

A complex can also be a component of a complex, e.g. [CMG-Pol epsilon complex](https://www.ebi.ac.uk/complexportal/complex/CPX-1556).

### Molecule sets

In some cases, such as ribosomal proteins, it is impossible to distinguish from which paralogous gene a protein is expressed. In these rare cases we have created sets that contain references to both UniProt instances of this protein. Sets have accessions of the type EBI-{0-9}. These sets are equivalent to the "defined sets" as used in [Reactome](https://reactome.org/): "A collection of well-characterized physical entities that are functionally indistinguishable for the purpose of Reactome annotation, e.g., a collection of isoforms of a protein that all mediate the identical metabolic reaction."

## Component Features

- Any feature is mapped to the underlying sequence, as given in the source database, and cross-referenced to InterPro when possible. 
- If a PTM is required for complex formation or activation it is curated as a feature and the effects detailed in the "Properties" section.
- Binding regions or residues within proteins known to directly interact within the complex are shown as linked features in the graphical views.
- Stoichiometry is added when known. Stoichiometry=0 (or empty field on the website and single component in the Complex Viewer) is used for components with no information about stoichiometry. It is common that stoichiometry is only know for some components in the same complex.

## Interaction Type

This is always 'Physical association', indicating that these proteins are present in the same complex.

## Experimental evidence

Every effort is made to link all entries to an experimental molecular interaction evidence but this is not always possible. We use the [Evidence and Conclusion Ontology (ECO)](http://www.evidenceontology.org/) to describe the type of evidence that was used to decide on the complex and link to primary molecular interaction databases where possible.

### Primary experimental evidence

When high quality evidence for the existence of this complex is present in an [IMEx database](http://www.imexconsortium.org/), [wwPDB](https://www.ebi.ac.uk/pdbe/) or [EMDB](https://www.ebi.ac.uk/pdbe/emdb/), an "exp-evidence"-type cross-reference to this database is added manually so that it may be downloaded in the same file as the complex. 

Complexes with "exp-evidence"-type cross-reference must also be annotated with ECO codes ECO:0000353 or ECO:0005543 (see below). 

### Additional experimental evidences from 3D structures (crystals and EM structures)

Additional, representative [wwPDB](https://www.ebi.ac.uk/pdbe/) and [EMDB](https://www.ebi.ac.uk/pdbe/emdb/) cross-references may be added. Structures may represent the whole complex (qualifier = identity) or a partial complex (qualifier = subset). 

### Evidence codes

The following [Evidence and Conclusion Ontology (ECO)](http://www.evidenceontology.org/) codes are used to indicate the strength of evidence that a complex exists: 

|ECO Code|Name|Description|Confidence Score|
|--------|----|-----------|----------------|
|[ECO:0000353](http://www.ebi.ac.uk/ols/ontologies/ECO/terms?obo_id=ECO:0000353)|physical interaction evidence used in manual assertion|Used when experimental evidence for the complexes exists in a single experiment. The complex must be cross-referenced to experimental data in either an IMEx database, wwPDB or EMDB.|![](https://raw.githubusercontent.com/Complex-Portal/complex-portal-documentation/master/assets/score_5_stars.png)|
|[ECO:0005543](http://www.ebi.ac.uk/ols/ontologies/ECO/terms?obo_id=ECO:0005543)|biological system reconstruction evidence by experimental evidence from mixed species used in manual assertion|Used when experimental evidence for the complexes exists in a single experiment but the constructs are derived from homologous gene products in different species. The complex must be cross-referenced to experimental in either an IMEx database, wwPDB or EMDB.|![](https://raw.githubusercontent.com/Complex-Portal/complex-portal-documentation/master/assets/score_5_stars.png)|
|[ECO:0005610](http://www.ebi.ac.uk/ols/ontologies/ECO/terms?obo_id=ECO:0005610)|biological system reconstruction evidence based on homology evidence used in manual assertion|Used when experimental evidence exists for a complex in one species and it is desirable to curate a similar complex in another species for which only limited experimental evidence exists. Sequences and number of genome-encoded components are fairly conserved but some divergence may be observed. The complex with the experimental evidence must be annotated with ECO:0000353 or ECO:0005543 and has to be cross-referenced with the qualifier = "inferred-from".|![](https://raw.githubusercontent.com/Complex-Portal/complex-portal-documentation/master/assets/score_4_stars.png)|
|[ECO:0005544](http://www.ebi.ac.uk/ols/ontologies/ECO/terms?obo_id=ECO:0005544)|biological system reconstruction evidence based on orthology evidence used in manual assertion|Used when experimental evidence exists for a complex in one species (e.g. human) and it is desirable to curate the same complex in another species for which only limited experimental evidence exists (e.g. mouse). Sequences are fairly conserved but some divergence may be observed and the number of genome-encoded components is identical. The complex with the experimental evidence must be annotated with ECO:0000353 or ECO:0005543 and has to be cross-referenced with the qualifier = "inferred-from".|![](https://raw.githubusercontent.com/Complex-Portal/complex-portal-documentation/master/assets/score_4_stars.png)|
|[ECO:0005546](http://www.ebi.ac.uk/ols/ontologies/ECO/terms?obo_id=ECO:0005546)|biological system reconstruction evidence based on paralogy evidence used in manual assertion|Used when experimental evidence exists for a complex and it is desirable to curate a similar complex in the same species for which only limited experimental evidence exists. Sequences and number of genome-encoded components are fairly conserved but some divergence may be observed. The complex with the experimental evidence must be annotated with ECO:0000353 or ECO:0005543 and has to be cross-referenced with the qualifier = "inferred-from".|![](https://raw.githubusercontent.com/Complex-Portal/complex-portal-documentation/master/assets/score_4_stars.png)|
|[ECO:0005547](http://www.ebi.ac.uk/ols/ontologies/ECO/terms?obo_id=ECO:0005547)|biological system reconstruction evidence based on inference from background scientific knowledge used in manual assertion|Used when no or only partial experimental evidence exists but the complex is generally assumed to exist. Functional studies or ligand binding evidence from pharmacological experiments are often used for the reconstruction of such complexes.|![](https://raw.githubusercontent.com/Complex-Portal/complex-portal-documentation/master/assets/score_3_stars.png)|
|[ECO:0007653](http://www.ebi.ac.uk/ols/ontologies/ECO/terms?obo_id=ECO:0007653)|automatically integrated combinatorial computational evidence used in automatic assertion|Used if a complex is predicted to exist from machine-learning data and is additionally supported by other evidence such as high confidence covariation data.|![](https://raw.githubusercontent.com/Complex-Portal/complex-portal-documentation/master/assets/score_2_stars.png)|
|[ECO:0008004](http://www.ebi.ac.uk/ols/ontologies/ECO/terms?obo_id=ECO:0008004)|machine learning method evidence used in automatic assertion|Used if a complex is predicted to exist from machine-learning data but has no additional supporting evidence.|![](https://raw.githubusercontent.com/Complex-Portal/complex-portal-documentation/master/assets/score_1_star.png)|

### Retrieval of references for curation evidence

- If experimental evidence is referenced (ECO:0000353 or ECO:0005543) the reference for the experimental data has to be retrieved from the primary databases (IntAct/IMEx, wwPDB, EMDB). The relevant PubMed reference is not necessarily listed in the cross-references.

- If a complex is inferred by homology (ECO:0005610 or a child term) the reference for the experimental evidence has to be retrieved from the primary database cross-reference (IntAct/IMEx, wwPDB, EMDB) of the complex it was inferred from. They are not necessarily listed in the cross-references.

- If is no known or curated experimental evidence is available for a complex (ECO:0005547) the complex has been inferred from several references or review(s) which are listed among the "additional literature" cross-references.

## Free text annotation

### Description

A brief, free-text description of the function of the complex, written in the same style as a UniProtKB/Swiss-Prot entry. For example "Required for processive DNA replication and may act as a replicative helicase during DNA synthesis. Plays a central role in S-phase genome stability.". 

### Properties

Details of physical properties of the complex. This may include details about the topology, varying (as opposed to absolute) stoichiometry, molecular weight and Stoke's radius of the complex. 

### Complex-assembly

Experimentally verified structural assembly e.g. homodimer, heterohexamer. Assemblies which have been computationally predicted are not included. 

### Disease

Only added when the disease state has been specifically linked to the protein when in the complex. 

### Ligands

One or more ligands transiently associated with this complex. They are usually linked to a [ChEBI](https://www.ebi.ac.uk/chebi/) identifier.

## Structured Annotations

All structured annotations are entered as database/controlled vocabulary cross-reference with an appropriate qualifier term.

### Gene Ontology

Annotation to [Gene Ontology](http://geneontology.org) terms indicates the function, process, location and component of the complex as a whole. The Function term, in particular, may not be true for all members of the complex, for example enzyme complexes will be annotated with a catalytic function term even when some subunits play only a regulatory role. 

### Enzymatic activity

Catalytical complexes are annotated with appropriate E.C. numbers linked to [IntEnz](https://www.ebi.ac.uk/intenz/) and reactions in [Rhea](https://www.rhea-db.org/).

### Additional literature

Articles covering further experimental or functional information and review articles are added and linked to [EuropePMC](http://europepmc.org/). 

### Pathway information

For human complexes, crosslinks to [Reactome](https://reactome.org/) put complexes into a pathway context. Note that the definition of a complex is different in Reactome and in many cases a one-to-many relationship exists. 

### Disease information

Cross references to the [Experimental Factor Ontology (EFO)](https://www.ebi.ac.uk/efo/) or their contributing databases (e.g. Orphanet, Human Phenotype Ontology) are added if a complex has been linked to a specific disease condition. 

### Drug target information

Cross-links to [ChEMBL](https://www.ebi.ac.uk/chembl/) are used to indicate complexes which have been used as drug targets. 

### External resources

<table>
    <thead>
        <tr>
            <th>Identifier</th>
            <th>Qualifier</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=5>
                <a href="https://www.ebi.ac.uk/emdb">EMDB</a><br>
                <a href="https://humap3.proteincomplexes.org">Hu.MAP3.0</a><br>
                <a href="http://www.ebi.ac.uk/pdbe">PDB</a><br>
                <a href="https://musicmaps.ai">MuSIC</a><br>
            </td>
            <td><a href="https://www.ebi.ac.uk/ols4/ontologies/mi/classes/http%253A%252F%252Fpurl.obolibrary.org%252Fobo%252FMI_0356" target="_blank">Identical object in an external resource</a></td>
            <td>Components in the Complex Portal complex and hu.MAP3.0 cluster or PDB/EMDB structure are identical. </td>
        </tr>
        <tr></tr>
        <tr>
            <td><a href="https://www.ebi.ac.uk/ols4/ontologies/mi/classes/http%253A%252F%252Fpurl.obolibrary.org%252Fobo%252FMI_2179" target="_blank">Subset</a></td>
            <td>A partial match with additional complex components in the Complex Portal complex. </td>
        </tr>
        <tr></tr>
        <tr>
            <td><a href="https://www.ebi.ac.uk/ols4/ontologies/mi/classes/http%253A%252F%252Fpurl.obolibrary.org%252Fobo%252FMI_2427" target="_blank">Complex-cluster</a></td>
            <td>Two or more complexes in the Complex Portal are a subset of a single hu.MAP3.0 entry with the difference being due to the clustering of paralogs in the hu.MAP3.0 complex.</td>
        </tr>
    </tbody>
</table>

### Links to External resources

* <a href="https://humap3.proteincomplexes.org">Hu.MAP3.0</a> - Fischer, S.N., Claussen, E.R., Kourtis, S., Sdelci, S., Orchard, S., Hermjakob, H., Kustatscher, G., Drew, K., 2024. hu.MAP3.0: Atlas of human protein complexes by integration of &gt; 25,000 proteomic experiments. https://doi.org/10.1101/2024.10.11.617930


* <a href="https://musicmaps.ai">MuSIC</a> - Qin, Y., Huttlin, E.L., Winsnes, C.F., Gosztyla, M.L., Wacheul, L., Kelly, M.R., Blue, S.M., Zheng, F., Chen, M., Schaffer, L.V., Licon, K., Bäckström, A., Vaites, L.P., Lee, J.J., Ouyang, W., Liu, S.N., Zhang, T., Silva, E., Park, J., Pitea, A., Kreisberg, J.F., Gygi, S.P., Ma, J., Harper, J.W., Yeo, G.W., Lafontaine, D.L.J., Lundberg, E., Ideker, T., 2021. A multi-scale map of cell structure fusing protein images and interactions. Nature 600, 536–542. https://doi.org/10.1038/s41586-021-04115-9


* <a href="https://www.proteomehd.net">ProteomeHD</a> - Kustatscher, G., Grabowski, P., Schrader, T.A., Passmore, J.B., Schrader, M., Rappsilber, J., 2019. Co-regulation map of the human proteome enables identification of protein functions. Nat Biotechnol 37, 1361–1371. https://doi.org/10.1038/s41587-019-0298-5

## Pairwise relationships

Protein-protein interaction data from external sources is displayed using gene names across the X and Y-axis in a heatmap. Below the heatmap is a correlation key ranging from 0-1, where 1 represents 100% co-expression between two proteins. Hover over the bricks of the heatmap for an exact score.

### Sources

* <a href="https://www.proteomehd.net">ProteomeHD</a> - Co-expression scores from ProteomeHD
* <a href="https://www.ebi.ac.uk/intact">IntAct</a> - Interaction scores from IntAct

## Complex Variants

If variant forms of a complex exist i.e. the same functional unit can exist in alternate forms with differing macromolecular composition, these are curated as separate objects. For example, PDGF can exist as a PDGF-A homodimer, PDGF-B homodimer, PDGF-AB heterodimer, PDGF-C homodimer and a PDGF-D homodimer. If the variants have well-accepted names, e.g. PDGF-AB, these may be used as the primary name. If not, then the recommended name is qualified by variant 1, variant 2 e.g. [TRAMP complex variant 1](https://www.ebi.ac.uk/complexportal/complex/CPX-1678).

## Versioning

A version is identified by a .x suffix (where x is a number) of the accession number. The version is included in the download files but not displayed on the website.

A complex receives a new version if its components change (adding or removing one or more components) or its function is redefined. 

## Obsoleted Complexes

If a complex has to be removed from the release database it is still available in previous release files accessible via our [ftp repository](http://ftp.ebi.ac.uk/pub/databases/intact/complex/current/) and marked as “on-hold” in our database. 

If the complex has been merged into an existing entry the accession number of the obsoleted complex is added to the complex it has been merged into as secondary ID allowing a user to still retrieve an entry. 

Secondary IDs are available in all download files while the website currently only displays the primary AC (e.g. CPX-3042 is now part of [CPX-2161](https://www.ebi.ac.uk/complexportal/complex/CPX-2161)).

## For curators

For trainined curators: here is the latest version of our [Complex Portal curation manual](https://raw.githubusercontent.com/Complex-Portal/complex-portal-documentation/master/assets/Manual_Complexes_curation.pdf).

Depending on your browser, you may have to right click on the link and choose "Save Link As" to download the file.

## Rules used to integrate the predicted hu.MAP3.0 complexes

<table><thead>
  <tr>
    <th>For</th>
    <th>Then</th>
  </tr></thead>
<tbody>
  <tr>
    <td>A hu.MAP complex is an exact match to existing manually curated complex</td>
    <td>Manually curated complex is master, add hu.MAP xref 'identity', put hu.MAP complex on-hold</td>
  </tr>
  <tr>
    <td>A hu.MAP complex is subset of existing manually curated complex</td>
    <td>Manually curated complex is master, add hu.MAP xref 'subset', put hu.MAP complex on-hold</td>
  </tr>
  <tr>
    <td>A hu.MAP complex is an exact match to planned new manually curated complex</td>
    <td>hu.MAP as master, ensure hu.MAP xref is retained as identitiy, ensure ECO is updated to releveant 3-5 star</td>
  </tr>
  <tr>
    <td>A hu.MAP complex is a subset of 1 new planned manually curated complex</td>
    <td>Start with hu.MAP as master, create new version, add hu.MAP xref as subset</td>
  </tr>
  <tr>
    <td>A hu.MAP complex is a subset of &gt;1 new manually curated complex</td>
    <td>Create new complexes, add hu.MAP xref as 'subset' to all, put hu/MAP complex on-hold</td>
  </tr>
  <tr>
    <td>If an existing complex will have update (components added/removed) that makes it a match to a hu.MAP complex or hu.MAP becomes an subset</td>
    <td>Manually curated complex stays as master, create new version, add hu.MAP xref, put hu.MAP complex on-hold.</td>
  </tr>
  <tr>
    <td>Manually curated Complex A:B and Complex A:C but hu.Map cluster is of A:B:C</td>
    <td>Add hu-MAP as xef to all curated entries, qualifier 'complex-cluster' and put hu.MAP entry on-hold.</td>
  </tr>
  <tr>
    <td>PRO-chain IDs</td>
    <td>Ignore, use the canonical form of the protein</td>
  </tr>
  <tr>
    <td>Isoforms</td>
    <td>Ignore, use the canonical form of the protein <br></td>
  </tr>
  <tr>
    <td>hu.MAP partial matches that can be annotated as a curated complex in its own right</td>
    <td>Claim ownership and annotate entry. These are partial matches from a first round mapping exercise, reviewed to be not a subset and have hu.MAP xref with an "identity" qualifier</td>
  </tr>
</tbody></table>


