# Anime Recommendation System

This project implements a recommendation system for anime based on multiple filters, such as:
genre, type, source, rating, and status.
The system is designed to help users find anime titles that match their preferences.

## Features
- Filter anime based on:
  - **Score**: Minimum rating score.
  - **Genres**: List of genres to match (e.g., Action, Comedy).
  - **Types**: Type of anime (e.g., TV, Movie).
  - **Source**: Original source of the anime (e.g., Manga, Light Novel).
  - **Rating**: Age rating (e.g., R - 17+).
  - **Status**: Current airing status (e.g., Finished Airing, Ongoing).
- Option to leave any parameter empty to match all available values for that category.

## Dataset

The dataset used for this anime recommendation system is sourced from Kaggle. You can download it from the following link:

[Kaggle Dataset: Anime Recommendations Dataset](https://www.kaggle.com/datasets/dbdmobile/myanimelist-dataset)

Once downloaded, place the dataset (`anime-dataset-2023.csv`) in the `data/` folder in the project directory.

Alternatively, you can download the dataset automatically by using the Kaggle API.

### Steps to download the dataset automatically:
1. Install the Kaggle API:
   ```bash
   pip install kaggle
   ```

2. Obtain your Kaggle API key from [Kaggle Account Settings](https://www.kaggle.com/account) by creating a new API token.
   This will download a `kaggle.json` file.

3. Place the `kaggle.json` file in the following directory:
   - **Linux/macOS**: `~/.kaggle/`
   - **Windows**: `C:\Users\<YourUsername>\.kaggle\`

4. Create a `data/` folder in the project directory:
   ```bash
   mkdir data
   ```

5. Run the following Python script to download the dataset:
   ```python
   import os
   os.system('kaggle datasets download -d dbdmobile/myanimelist-dataset -p ./data/')
   ```


## How to Use

1. Clone this repository:
   ```bash
   git clone https://github.com/S19Deen/Python_Projects.git
   ```

2. Navigate to the Anime Recommendation System folder:
   ```bash
   cd Python_Projects/Anime\ Recommendation\ System
   ```

3. Install necessary dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `data/` folder and place the `anime-dataset-2023.csv` file inside it:
   ```bash
   mkdir data
   ```

5. Run the recommendation function by calling `anime_recommendation_fun` with the desired parameters:
   ```python
   import pandas as pd
   from anime_recommendation import anime_recommendation_fun

   # Load the dataset
   anime_data = pd.read_csv('data/anime-dataset-2023.csv')

   # Get recommendations based on filters
   recommendations = anime_recommendation_fun(anime_data, 
                                              score=8.0, # Leave empty for all scores
                                              genres=['Action'], # Leave empty for all genres
                                              types=['TV'], # Leave empty for all types
                                              source=['Original'], # Leave empty for all sources
                                              rating='PG-13 - Teens 13 or older',  # replace with None for all ratings
                                              status='Finished Airing')  # replace with None for all statuses

   # Print the recommendations
   for anime_id, anime in recommendations.items():
       print(f"Anime ID: {anime_id}")
       print(f"Name: {anime['Name']}")
       print(f"Score: {anime['Score']}")
       print(f"Genres: {anime['Genres']}")
       print(f"Type: {anime['Type']}")
       print(f"Rating: {anime['Rating']}")
       print(f"Status: {anime['Status']}")
       print("-" * 40)
   ```
## Filter Options
- **Score**: Minimum rating score (e.g., 8.0). The score ranges from 0.0 to 10.0.
- **Genres**: Action, Adventure, Avant Garde, Award Winning, Boys Love, Comedy, Drama, Ecchi, Erotica, Fantasy, 
              Girls Love, Gourmet, Hentai, Horror, Mystery, Romance, Sci-Fi, Slice of Life, Sports, Supernatural, Suspense
- **Types**: Movie, Music, ONA, OVA, Special, TV
- **Sources**: 4-koma manga, Book, Card game, Game, Light novel, Manga, Mixed media, Music, Novel, Original, 
              Other, Picture book, Radio, Visual novel, Web manga, Web novel
- **Ratings**: G - All Ages, PG - Children, PG-13 - Teens 13 or older, R - 17+ (violence & profanity), 
              R+ - Mild Nudity, Rx - Hentai
- **Statuses**: Currently Airing, Finished Airing, Not Yet Aired

## Contributing

Feel free to fork the repository, make changes, and create pull requests. Contributions are welcome!

## Acknowledgments
- Kaggle for the dataset: [myanimelist-dataset](https://www.kaggle.com/datasets/dbdmobile/myanimelist-dataset) contributed by [dbdmobile](https://www.kaggle.com/dbdmobile)
- Pandas library for efficient data manipulation

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Made with Jupyter Notebook by [S19Deen](https://github.com/S19Deen)
