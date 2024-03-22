# Generating tags using Topic Modeling

## Goal: 
The goal of this project is to expose myself in the NLP section of ML, where I learn to implement various NLP techniques like topic modeling using ML to generate tags based on a summary of a Vietnamese dish recipe. 

## Tools:
Data processing: pandas, numpy

Web scraper: requests, BeautifulSoup

Deep learning framework: tensorflow, Hugging Face's transformers, scikit-learn, nltk

Visualization: matplotlib

## Process:
1. Initialization and Data Embedding

• Transformed the recipe's description into a 512-dimensional space via embedding 

2. Determine the optimal number of topics

• Visualized the optimal number of topics to be genereated using matplotlib's elbow plot

• Fit a KMeans clustering algorithm with a range of cluster sizes

• Plot the inertia (within-cluster sum of squares) to find the "elbow point" where the addition of more clusters doesn't significantly improve the model's fit

4. Cosine similarity calculation

• Calculates the cosine similarity between any two given vectors to assess their similarity in the embedded space (closer to 1 if a match and closer to 0 if different)

5. Extracting keywords for topics

• Computes the cosine similarity between the word embeddings and the centroid of a topic's cluster to select topics that are closer to the centroid

6. Create topics

• Return a list containing the topics that are closest to the centroid of a topic's cluster

## Future work:
This project serves as a beginner's introduction to the world of NLP and how to generate tags using techniques like Topic Modeling. There's definitely more room to use these tags and other information in the dataframe for future uses like a recipe generator, where the user can prompt a request and the application recommends Vietnamese food recipes for them based on tags in their prompt.
