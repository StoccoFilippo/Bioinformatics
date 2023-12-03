
# Color a PDB File Based on Sequence Identity

I'm currently working on a Python script that utilizes data from a multiple sequence alignment to color-code amino acids in a PDB structure. The script calculates amino acid frequencies and conservation, enabling the visualization of conservation patterns. This information is invaluable for identifying conserved residues, giving insights over the possible role in important roles (e.g interaction with other subinits, active sites, structural...). Additionally, the script generates a frequency table, which serves as the basis for creating a Multiple Sequence Alignment (MSA) visualization using the `pyMSAviz` Python package.

## Example:
Using BLAST, 500 sequence of the studied enzyme was obtained. A Multiple Sequence Alignment (MSA) was compiled using Clustal algorithm. The obtained fasta sequence is used as imput for the pyton script. The frequency of the most prevalent amino acid for each position has been determined as displayed in the following table.

![image](https://github.com/StoccoFilippo/IdentityPDBVisualization/assets/148588396/b38ecba0-4e71-4428-ae64-606a134b9971)

Subsequently, the PDB file was modified in the `bf` field. In PyMol, amino acids with an identity lower than 80 were selected (select br. b<80) and colored in gray. A gradient from blue to red was used to color amino acids with higher identity (spectrum b, blue_red, minimum=80, maximum=100), resulting in the following image:

![image](https://github.com/StoccoFilippo/IdentityPDBVisualization/assets/148588396/6a6339c4-c337-4110-8415-5f82abc8ea20)

![pMMOidentitysctivesite](https://github.com/StoccoFilippo/IdentityPDBVisualization/assets/148588396/1d7885bc-965a-4762-accd-6651243d0240)

Finally, the Multiple Sequence Alignment (MSA) visualization of the desired range (in this case position 100-160) is obtained as shown here:

![image](https://github.com/StoccoFilippo/IdentityPDBVisualization/assets/148588396/da4c53f0-992a-484a-8802-c51cca84c848)

Here is an example of a metalloenzyme with three putative active sites (Cu_A, Cu_B, and Cu_C). Cu_A exhibits low conservation, suggesting it is likely not an active site.
![pMMOidentitysctivesite](https://github.com/StoccoFilippo/IdentityPDBVisualization/assets/148588396/1d7885bc-965a-4762-accd-6651243d0240)

