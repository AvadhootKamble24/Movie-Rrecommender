# Movie Recommendations 

This repository contains the code for a Movie Recommender System using data from the TMDB 5000 movies and credits dataset. The project demonstrates data preprocessing, feature engineering, and building a recommendation engine using various machine learning techniques.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Data](#data)
- [Preprocessing](#preprocessing)
- [Feature Engineering](#feature-engineering)
- [Building the Model](#building-the-model)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/movie-recommender.git
   cd movie-recommender
   ```

2. Create and activate a virtual environment (optional but recommended):
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. Install the required packages:
   ```sh
   pip install -r requirements.txt
   ```

## Usage

1. Ensure you have the datasets (`tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`) in the project directory.
2. Run the Jupyter notebook:
   ```sh
   jupyter notebook movie_recommender.ipynb
   ```

## Data

The datasets used in this project are:

- **tmdb_5000_movies.csv**: Contains information about movies such as budget, genres, homepage, original language, overview, popularity, production companies, release date, revenue, runtime, status, tagline, title, vote average, and vote count.
- **tmdb_5000_credits.csv**: Contains information about the cast and crew of the movies.

## Preprocessing

Data preprocessing steps include:

- Merging the movies and credits datasets on the movie title.
- Handling missing values by dropping rows with null values in essential columns.
- Extracting relevant features such as genres, keywords, cast, and crew.
- Converting textual data into lists of keywords for easier manipulation.

## Feature Engineering

Feature engineering steps include:

- Creating a function to extract the names of genres, keywords, cast, and crew members.
- Limiting the cast to the top 3 members.
- Extracting the director's name from the crew.
- Creating a 'tags' column that combines all relevant textual information.
- Removing spaces from the tags to maintain consistency.
- Converting all text to lowercase for uniformity.

## Building the Model

The recommendation system is built using:

- A text-based similarity measure.
- Vectorization of the 'tags' column using TF-IDF.
- Calculation of cosine similarity between movie vectors.
- Providing movie recommendations based on similarity scores.

## Results

The system provides movie recommendations based on the similarity of movie attributes. Detailed results and performance metrics are available in the notebook.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any enhancements or bug fixes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
