# A-Deep-Learning-Approaach-to-Biodiverrsity-Clustering-Wildlife-Images-in-Yasun-Using-CNNs
Python code for clustering over 100,000 wildlife images from Yasuní National Park using CNNs. This project highlights deep learning applications in biodiversity monitoring and conservation
1. ExtraccioncaracteristicasResnet152.ipynb
Description:

This notebook handles the feature extraction process using the ResNet-152 model. It's set up to process images by removing the last layer of the network to use it as a feature extractor rather than for classification.
The notebook reads metadata from a JSON file and image files from a specified directory, then processes each image through ResNet-152 to extract features, which are then stored in a JSONL file. Relation to Article:
This notebook directly supports the article's methodology by preparing the image data for clustering analysis through feature extraction, a critical step in analyzing images using machine learning.

2. tsne-visualizacionklusters152.ipynb
Description:

This notebook performs t-Distributed Stochastic Neighbor Embedding (t-SNE) to reduce the high-dimensional data from the extracted features into a two-dimensional space for visualization.
It uses K-Means clustering on the features to identify patterns before applying t-SNE for better visualization and understanding of the data clusters. Relation to Article:
It complements the article by providing visual insights into how well the features cluster and helps in identifying the optimal number of clusters, which is crucial for the analysis and conclusions of the study.

3. FinalGmm.ipynb
Description:

This notebook applies a Gaussian Mixture Model (GMM) to the features extracted in the ExtraccioncaracteristicasResnet152.ipynb notebook. It evaluates the clustering using silhouette scores to assess the effectiveness of the clustering.
It also uses t-SNE to visualize the clustering results and assigns representative images to each cluster, enhancing interpretability. Relation to Article:
Essential for the article as it finalizes the clustering process and provides both a quantitative and qualitative assessment of the clusters, linking directly back to the biodiversity analysis discussed in the article.

4. cutbeforextraction-Copy1.ipynb
Description:

This notebook is set up to demonstrate preprocessing steps on images before feature extraction. It includes cropping based on detection bounding boxes and applies image transformations as per the requirements of the ResNet model.
It visually compares the original, cropped, and transformed images to demonstrate the preprocessing effects. Relation to Article:
Provides a detailed look at the preprocessing steps that prepare the images for feature extraction, illustrating the initial stages of the image processing pipeline that precedes the feature extraction discussed in the article.

5.Metadata and jsons merge.ipynb

This notebook extracts metadata from the images and utilizes the MegaDetector to generate the JSON file that will be used in subsequent steps for feature extraction
