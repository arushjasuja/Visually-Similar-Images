# Visually-Similar-Images
Finding Visually Similar Garments for an Input Garment

Every image in the dataset is preprocessed so that they can be fed to a pretrained model. InceptionV3 trained on ImageNet data is used here because it has a good tradeoff between accuracy and speed performance. The last dense layer of this pretrained model is removed so it can be used to extract feature representations.
These vector representations can be used to calculate similarity between two images. Cosine Similarity is used here for this purpose. The most similar images are then displayed.

After the vector representations are formed, if the database is updated with new images. The encoding is performed with the new images only. The feature representations for existing images in the previous run are not extracted again.

How to Run:
  The file path for the query image needs to be set and the code needs to be run. The embeddings file can be found at the link below.
  https://drive.google.com/file/d/1eaYSMyNm9IPTJzmr4kf-jOaVruMoTkjb/view?usp=sharing
  The file can be executed on google colab or jupyter

Future Scope:
1. Exception handling can be used to deal with possible edge cases such as, ignoring corrupt images in the database if any
2. Finding similar images is computationally expensive, the problem gets worse as the size of data increases. Services like Google Vertex AI Matching Engine, IO Similarity Search, Pinecone, Milvus can be used to deal with this.
3. An encoder - bridge - decoder modelling approach can also be useful
4. Euclidean Distance can also be used
5. Different Pre-trained model can be used
