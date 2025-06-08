# Unsupervised-DL-image-classifier-routine
A general-purpose Jupyter notebook designed for unsupervised image classification. It does not contain specific results, but instead provides a well-tested and reusable workflow for future image clustering tasks.

The routine consists of the following steps:
1. Gather images from a source directory or a list of filepaths, preprocess them (resize, brightness, contrast) and copy to a local folder. 
2. Use pretrained CNNs (InceptionV3 or EfficientNetV2B0) to extract features from each image. For this purpose, the output layer of these networks has been removed, given that in our case, we do not want to assign classes to the images. Both CNNs have been pretrained on imagenet. 
3. Use features assigned to each image to cluster the images using either K-means or DBSCAN. Depending on the specific problem, one could work better than the other. 
4. Images get sorted in folders by their cluster number and some qualitative metric of the clustering using the Silhouette plot is calculated. 
