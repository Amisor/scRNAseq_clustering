# scRNAseq_clustering

The brain, a highly complex organ with diverse cell types essential for neural function, connectivity, and physiology, serves
as an excellent case for evaluating cell classification methods. Accurate classification of brain cell types can advance our
understanding of neurobiology and neurological disorders. In this study, single-cell classification is perform in mouse brain
tissue. Extensive Quality Control (QC) metrics helped us to to ensure that only high-quality cells and informative genes are
included. 94.4% of the cells and 79.3% of the genes were retained for the modeling process. A Support Vector Machine
(SVM) served as a benchmark model. CellTypist, scANVI, and Cell BLAST, designed for single-cell RNA sequencing
data, were also employed, reflecting the diversity of computational approaches encompassing traditional machine learning,
generative frameworks, and similarity-based methods. Overall, the benchmarking SVM performed well in the classification
task, achieving a high accuracy and precision across different categories; CellTypist and scANVI performed equivalently
to SVM in terms of prediction quality, and performed equally across the cell types without discrepancies; Cell BLAST
performed less well, yet its ability to classify cells as "ambiguous" and "rejected" may provide new insights into novel and
rare cell type discoveries.

# Directories 

## data

Contains files related to the brain dataset from the Tabula Muris project. 
The dataset includes gene expression data, 
dimensionality reduction visualizations, and metadata, 
along with files processed for quality control and doublet removal.


* `brain_counts.csv.gz`: compressed file containing the gene expression matrix of 3,401 cells × 23,433 genes for the brain dataset.

* `brain_embeddings.h5ad.gz`: compressed file containing dimensionality reduction visualizations used for clustering and visualization.

* `brain_metadata.csv.gz`: compressed file containing metadata for the brain dataset, including cell type annotations and experimental conditions.

* `brain_qc.h5ad.gz`: compressed file containing the brain dataset after quality control with doublets removed.

* `brain_raw.h5ad.gz`: compressed file containing the raw brain dataset, including steps for doublet detection and removal.

## notebooks 
* `01_02_EDA_and_QC.ipynb`: performs exploratory data analysis, preprocessing with SCANPY, and quality control metrics.

* `03_doublets_mito_rib_visualization.ipynb`: covers doublets removal and data visualization by ontology class.

* `04_SVM_benchmark.ipynb`: implements a support vector machine as a benchmarking model.

* `05_CellTypist.ipynb` : uses CellTypist for cell classification.

* `06_Cell_BLAST.ipynb`: applies Cell BLAST for cell classification.

* `07_scANVI.ipynb`: utilizes scANVI for cell classification.

# Notes

All files are compressed to save space and can be decompressed using tools like gzip or similar utilities.

The .h5ad format is compatible with popular single-cell analysis tools such as Scanpy.

Ensure you have sufficient memory and storage to handle these files, as they may be large after decompression.


# References

The Tabula Muris Consortium. Single-cell transcriptomics of
20 mouse organs creates a tabula muris. Nature, 562:367–372, 2018.