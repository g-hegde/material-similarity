# material-similarity

A primer on computational materials discovery. The goal here is to demonstrate materials discovery using accessible but relevant examples. A materials dataset is first created by querying the Materials Project through pymatgen. Next, Valence Electronic Configuration (VEC) of materials in the database is used to create features. Unsupervised machine learning is performed on the datqaset to cluster materials together and find materials that are similar to targets. As an example, unary, binary and ternary materials that are electronically similar to Copper are mined and counterintuitive results are obtained. In another example, the discovery of nitride materials with VEC closest to copper are also mined for their potential use in diffusion barriers.

# Table of Contents  
[Packages Needed](#packages-needed)  
[File Description](#file-description)  
[Files Needed](#files-needed)  
[Usage Examples](#usage-examples)  

<a name="packages-needed"></a>  
## Packages Needed  

* pymatgen  
* matminer  
* pandas  
* scikit-learn  
* numpy  

<a name="file-description"></a>  
## File Description  

1. materials_similarity.ipynb - Main Jupyter Notebook containing the blog post along with python code and illustrative examples.  
2. \*.jpg and \*.png  - Image files used in the Jupyter Notebook.  
3. README.md - this file.  

<a name="files-needed"></a>     
## Files Needed  

None apart from above

<a name="usage-examples"/></a>  
## Usage examples  

Executed in Jupyter Notebook


