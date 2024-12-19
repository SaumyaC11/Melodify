# Melodify - Music Similarity through Embedding and Metadata

## Overview
Melodify is a music recommendation system designed to address the cold start problem and provide recommendations for less popular artists. The system integrates data from the Last.fm API and the Million Song Dataset Subset to generate comprehensive insights and enhance music discovery.

## Datasets
1. **Million Song Dataset Subset**: This dataset includes song-level audio features such as:
   - Danceability
   - Bar confidence
   - Segment loudness
   
   The songs are converted into NumPy arrays to facilitate efficient computation and analysis.

2. **Last.fm API**: This dataset provides metadata for artists and songs, including:
   - Artist popularity
   - Play count
   - Listener count
   - Similar artists

## Data Visualizations
1. **Playcount Distribution**: Distribution of play counts across artists and albums in the Last.fm dataset.
2. **Top 10 Artists**: Analysis of the top 10 artists based on play count, listener count, and engagement ratio.
3. **User Tags**: Visualization of popular tags assigned to specific songs or artists on Last.fm.
4. **Listeners vs. Players**: Trend analysis showing the relationship between listener count and play count.
5. **Country-wise Distribution**: Geographical distribution of users present in the Last.fm dataset.

## Exploratory Data Analysis (EDA)
1. **Data Cleaning**:
   - Converting columns to appropriate data types.
   - Handling missing values by removing columns and rows with excessive NaN values and replacing others with NaN where applicable.

2. **Feature Engineering**:
   - Generating new features for use in machine learning models.
   - Creating embeddings for songs, tags, and metadata.

## Machine Learning Models and Data Mining Techniques
1. **Clustering Songs using Audio Features**:
   - Songs are converted into embeddings using a Convolutional Neural Network (CNN) for clustering.

2. **Tag-based Song Clustering**:
   - Tags are converted to embeddings using Sentence-BERT (SBERT).
   - Clustering is performed using XGBoost to group songs based on tag embeddings.

3. **Similarity Analysis Using RNN**:
   - A Recurrent Neural Network (RNN) is used to understand and measure the similarity between songs.

4. **Feature Importance with Random Forest**:
   - A Random Forest model is used to identify the most important features contributing to song similarity and clustering.

5. **Tag Embeddings with Word2Vec**:
   - Tags are converted into embeddings using Word2Vec, enabling better semantic understanding of tag relationships.

6. **Graph Embedding for Tags, Artists, and Tracks**:
   - A graph-based approach is used to create embeddings for relationships between tags, artists, and tracks, enabling deeper contextual understanding.

## Key Features
- **Cold Start Problem**: Recommends songs and artists even with limited interaction data.
- **Multi-source Data**: Combines rich metadata from Last.fm with detailed audio features from the Million Song Dataset.
- **Comprehensive Embedding Models**: Uses CNNs, RNNs, SBERT, Word2Vec, and graph embeddings to derive insights from a variety of features.
- **Data Visualization**: Provides visual insights into artist engagement, user trends, and tag-based popularity.

## Conclusion
Melodify leverages the power of embeddings, metadata, and machine learning to create a robust music recommendation system. By integrating data from Last.fm and the Million Song Dataset, Melodify offers personalized recommendations, especially for less popular artists, overcoming the cold start challenge.

