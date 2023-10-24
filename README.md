# single-cell-analysis
Single cell RNA seq analysis of pre-neoplastic and normal breast cancer data sets for their macrophage cluster

The aim of this project is to find single cell rna seq data sets of breast tissue in normal or high-risk women (pre-neoplastic and no tumour samples). Then subset the macrophage clusters and see if we can further cluster the macrophages to their sub-populations. If that works, I would ideally perform more downstream analysis

 

BPal-Analysis-1
-------------------
Obtained Bhupinder Pal data set (https://doi.org/10.15252/embj.2020107333)

I obtained 17 normal and pre-neoplastic data set from GSE161529 . I then followed the Seurat v3 clustering vignette (https://satijalab.org/seurat/articles/pbmc3k_tutorial) and this tutorial https://www.youtube.com/watch?v=5HBzgsz8qyk&list=PLJefJsd1yfhagnkss5B1YCsHaH0GWQfFT&index=3&pp=iAQB)

I took each data set, then performed QC and filtering for each data set. Normalization and scaling were done using SCTransform (suggested by Conor in my lab). 

I then clustered each data set. I used FindAllMarkers to find the genes expressed by each cluster. I then identified which clusters highly express macrophage genes

Of the 17, 11 showed me clusters with macrophage genes. I subset each of these clusters and then integrated them based on this tutorial and Seurat v3 vignette

I could not cluster the integrated data because of how low the number of cells present from each data set that was integrated. I followed this tutorial for integration (https://www.youtube.com/watch?v=HrbeaEJqKcY&list=PLJefJsd1yfhagnkss5B1YCsHaH0GWQfFT&index=4&pp=iAQB)
