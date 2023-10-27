
# Color a PDB File Based on Sequence Identity

I'm currently working on a Python script that utilizes data from a multiple sequence alignment to color-code amino acids within a PDB structure. The script calculates amino acid frequencies and conservation, enabling the visualization of conservation patterns. This information is invaluable for identifying conserved residues and their specific roles, such as their involvement in catalytic sites or interactions with other subunits. Additionally, the script generates a frequency table, which serves as the basis for creating a Multiple Sequence Alignment (MSA) visualization using the `pyMSAviz` Python package.

## Example:
We obtained a Multiple Sequence Alignment (MSA) through BLAST. The frequency of the most prevalent amino acid for each position has been determined and is presented in the following table.

![image](https://github.com/StoccoFilippo/IdentityPDBVisualization/assets/148588396/e5158e36-baf5-43a9-8792-bbd145208a4d)

Subsequently, the PDB file was modified in the `bf` field. In PyMol, amino acids with an identity lower than 80 were selected and colored in gray. A gradient from blue to red was used to color amino acids with higher identity, resulting in the following image:

![image](https://github.com/StoccoFilippo/IdentityPDBVisualization/assets/148588396/6a6339c4-c337-4110-8415-5f82abc8ea20)

Finally, the Multiple Sequence Alignment (MSA) visualization is obtained as shown here:

![image](https://github.com/StoccoFilippo/IdentityPDBVisualization/assets/148588396/da4c53f0-992a-484a-8802-c51cca84c848)
