# material-similarity

Explore computational materials discovery using elementary electronic structure.

# Table of Contents  
[Motivation](#motivation)  
[Project Overview](#overview)  
[Results Summary](#results)  
[Libraries Needed](#packages-needed)  
[File Description](#file-description)  
[Usage Examples](#usage-examples)  

<a name="motivation"></a>  
## Motivation  
The goal of this project is to explore computational materials discovery using accessible but relevant examples. I chose this project owing to it's relevance in my own field of work (computational material science). I also wanted to get more familiar with two excellent python packages for materials data exploration - MatMiner and PyMatgen. Broadly speaking, I wanted to explore how very simple concepts like average electronic structure can be used to group materials together. Having grouped materials, the aim was to find materials that are electronically similar to materials that one may be interested in.

<a name="overview"></a>  
## Project Overview  

The following questions are sought to be answered through the project. 

1. When materials are represented on the basis of their average Valence Electronic Configuration (VEC), what is the optimum number of clusters that they can be grouped into?  
2. What materials are represented by cluster centers? Alternately, what unary material/materials are closest to cluster centers?  
3. Does the grouping make intuitive sense - i.e. are the cluster centers sufficiently far away from each other on the basis of chemical intuition?  
4. Given a target material, say Copper, what is the material (unary, binary and ternary respectively) whose VEC most closely resembles that of Copper? Performing such an analysis could be useful for finding replacements for <a href = "https://en.wikipedia.org/wiki/Copper_interconnects"> Copper interconnects</a> in microprocessors.  
5. Given a target material, say Copper, what is the (binary and ternary) nitride material whose average VEC most closely resembles that of Cobalt?  Performing such an analysis could be useful for finding suitable diffusion barrier materials for Copper interconnects.  

A materials dataset is first created by querying the Materials Project through pymatgen. Next, Valence Electronic Configuration (VEC) of materials in the database is used to create features. Unsupervised machine learning (k-means clustering) is performed on the dataset to cluster materials together and find materials that are similar to targets. As an example, unary, binary and ternary materials that are electronically similar to Copper are mined and counterintuitive results are obtained. In another example, nitride materials with VEC closest to copper are also mined for their potential use in diffusion barriers. 

<a name="results"></a>
## Results summary  

1. 4-6 clusters is found to be an optimum number of groups of similar materials.  
2. This analysis found Cr, Si, K and S as materials representing cluster centers. The list is non-exhaustive since there are a number of materials having exactly the same VEC as the elements above.  
3. The grouping does make intuitive sense since the elements represent very different types of materials - transition metal, alkali metal, semiconductor and non-metal.  
4. Besides the intuitively  obvious examples of Silver and Gold, HgPd and ZnPd are discovered to be most similar to Cu in terms of their VEC.  
5. Mo3Pd2N was found to be the Nitride with VEC closest to Cu.  

<a name="packages-needed"></a>  
## Libraries Used  

* pymatgen  
* matminer  
* pandas  
* scikit-learn  
* numpy  

<a name="file-description"></a>  
## File Description  

1. materials_similarity.ipynb - Main Jupyter Notebook containing the python code and illustrative examples of materials discovery.  
2. \*.jpg and \*.png  - Image files used in the Jupyter Notebook.  
3. README.md - this file.  

<a name="usage-examples"/></a>  
## Usage examples  

Execute accompanying Jupyter Notebook after installing required packages.


