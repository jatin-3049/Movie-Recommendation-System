# Movie-Recommendation-System
**Project Overview**
This is a content-based movie recommendation system that suggests similar movies based on features like genres, keywords, cast, and crew. The system uses the TMDB 5000 dataset containing information about 4809 movies.

**Data Preprocessing**

**1. Initial Setup**

**Installed dependencies:** scikit-learn and nltk for text processing and machine learning capabilities

**Imported libraries:** pandas for data manipulation, ast for literal evaluation of strings

**2. Data Loading**

Loaded two datasets:

**tmdb_5000_movies.csv:** Contains movie details (budget, genres, keywords, etc.)

**tmdb_credits_reduced.csv:** Contains cast and crew information

Merged these datasets on the 'title' column to create a comprehensive movie dataset

**3. Feature Selection**
**Selected relevant columns:** ['id', 'title', 'genres', 'keywords', 'cast', 'crew']

**Why these columns?**

Kept only the most relevant features for content-based recommendation

Removed financial data (budget, revenue) as they don't contribute to content similarity

Removed technical details (runtime, languages) that don't affect user preferences

Removed popularity/vote metrics to focus on intrinsic movie features rather than popularity

**4. Data Transformation**
**Genres and Keywords Processing**
Original format: String representation of list of dictionaries (e.g., [{"id": 28, "name": "Action"}, ...])

Converted to: List of genre/keyword names (e.g., ['Action', 'Adventure'])

**Why this transformation?**

Extracted only the meaningful names for recommendation

Simplified complex nested structure for easier processing

Prepared data for vectorization in later steps
