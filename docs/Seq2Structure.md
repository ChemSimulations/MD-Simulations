### Convert a Sequence to 3D Structure

#### Objectives
```
1. Convert a Fasta Sequence to 3D structure using SWISSPDB, Alphafold, and I-TASSER.
```


#### SWISSPDB-EXPASCY
1. This is an online tool used to convert a sequence to 3D structure
2. Models are computed by the SWISS-MODEL server homology modelling pipeline (Waterhouse et al.) which relies on ProMod3 (Studer et al.), an in-house comparative modelling engine based on OpenStructure (Biasini et al.).
3. Input a sequence in the box provided, and click on search templates to select a suitable template for the input sequence.
4. The server will give a Three dimesnional structure in few minutes.
5. SWISSPDB-EXPASCY can only model Proteins this cannot be used to model **DNA** or **RNA**
#### Link to the server
 [SwissPDBexpacy](https://swissmodel.expasy.org/interactive)
 
 [Tutorial](https://swissmodel.expasy.org/docs/examples)


 #### ALPHAFOLD-3
 1. ALPHAFOLD can predict the structures of **Protein**, **DNA** and **RNA** and common ligands such as ADP, ATP, NAD, NADPH.
 2. Upload the sequence in the checker box of alphafold server.
 3. Maximum 20 jobs can be submitted in a day and upto 5000 tokens
 4. [AlphaFold](https://alphafoldserver.com/)

#### I-TASSER
1. I-TASSER (Iterative Threading ASSEmbly Refinement) is a hierarchical approach to protein structure prediction and structure-based function annotation
2. It first identifies structural templates from the PDB by multiple threading approach LOMETS, with full-length atomic models constructed by iterative template-based fragment assembly simulations.
3. This server can only be used to model 3D structure of proteins.
4. I-TASSER [https://zhanggroup.org/I-TASSER/]
    
 












#### References
1. Waterhouse A, Bertoni M, Bienert S, Studer G, Tauriello G, Gumienny R, Heer FT, de Beer TAP, Rempfer C, Bordoli L, Lepore R, Schwede T
SWISS-MODEL: homology modelling of protein structures and complexes. Nucleic Acids Res 46, W296-W303. (2018) PubMed logo29788355 DOI logo10.1093/nar/gky427
2. ProMod3 Studer G, Tauriello G, Bienert S, Biasini M, Johner N, Schwede T ProMod3 - A versatile homology modelling toolbox.PLOS Comp Biol 17(1), e1008667. (2021)
PubMed logo33507980 DOI logo10.1371/journal.pcbi.1008667
3. OpenStructure (OST) Biasini M, Schmidt T, Bienert S, Mariani V, Studer G, Haas J, Johner N, Schenk AD, Philippsen A, Schwede TOpenStructure: an integrated software framework for computational structural biology. Acta Cryst 2013. (2013) PubMed logo23633579 DOI logo10.1107/S0907444913007051
