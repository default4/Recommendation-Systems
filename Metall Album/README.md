# Death Metal Album Recommendation System

## Project Overview

This project aims to build a content-based recommendation system for death metal albums. The recommendation system suggests similar albums based on various features such as the band's country of origin, status, genre, theme, the year the album was released, and the average review score.

## Datasets

The project utilizes three datasets from (https://www.kaggle.com/datasets/zhangjuefei/death-metal):

1. **albums.csv**
   - Contains information about death metal albums, including the album ID, band ID, title, and release year.
   
2. **bands.csv**
   - Provides details about death metal bands, including the band ID, name, country of origin, status, year formed, genre, theme, and active years.
   
3. **reviews.csv**
   - Includes reviews of death metal albums with review ID, album ID, title, score, and content.

## Methodology

The project follows these steps:

### 1. Data Preprocessing
   - The datasets are loaded and merged to form a comprehensive view of each album.
   - Missing or inconsistent data is handled appropriately.
   - The average review score for each album is computed.

### 2. Feature Engineering
   - Relevant features for the recommendation system are selected and preprocessed.
   - Categorical features are one-hot encoded, and numerical features are normalized.

### 3. Similarity Computation
   - Cosine similarity is calculated between albums based on the preprocessed features.
   - A similarity matrix is created, storing the similarity scores between each pair of albums.

### 4. Recommendation Generation
   - Given an album, the system recommends the top N most similar albums based on the similarity matrix.

## Visualizations

Various visualizations are created to understand the distribution and relationships among features, including:
   - Distribution of average review scores.
   - Number of albums released each year.
   - Distribution of albums by country.
   - Distribution of albums by genre.
   - Distribution of albums by band status.

## Results

The recommendation system successfully suggests similar albums for a given input album, based on content similarity. The results can be further refined and validated with additional user interaction data.

## Future Work

- Incorporate user interaction data to build a hybrid recommendation system.
- Evaluate the recommendation system using user feedback or implicit user interaction data.
- Explore additional features and fine-tune the model for better recommendations.

## Usage

To use the recommendation system, input the album ID for which you want recommendations and specify the number of recommendations desired. The system will output the top N most similar albums along with relevant details.

## Dependencies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
