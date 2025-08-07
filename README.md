# alx-project-0x14

## API Overview

The **MoviesDatabase API** is a powerful and comprehensive API providing detailed and updated information about movies, TV shows, and actors. It supports over 9 million titles and 11 million cast and crew members. It includes data like:

- Movie and series details
- YouTube trailer URLs
- Ratings, awards, and biographies
- Upcoming releases
- Actor profiles
- Season and episode data for TV series

All endpoints return a consistent structure centered around a `results` object. Many queries are customizable through optional parameters.

## Version

This documentation refers to the **latest public version** of the MoviesDatabase API. The version is not explicitly numbered in the documentation.

## Available Endpoints

### Titles

- **GET /titles** – Retrieve a list of titles based on filters or sorting.
- **GET /x/titles-by-ids** – Get multiple titles using an array of IMDb IDs.
- **GET /titles/{id}** – Get details for a specific title.
- **GET /titles/{id}/ratings** – Get ratings and votes for a title.
- **GET /titles/x/upcoming** – Retrieve upcoming titles.

### Series and Episodes

- **GET /titles/series/{id}** – List episodes of a series with episode and season numbers.
- **GET /titles/seasons/{id}** – Get total number of seasons for a series.
- **GET /titles/series/{id}/{season}** – List episodes of a specific season.
- **GET /titles/episode/{id}** – Get detailed information about an episode.

### Search

- **GET /titles/search/keyword/{keyword}** – Search titles using a keyword.
- **GET /titles/search/title/{title}** – Search titles by exact or partial title.
- **GET /titles/search/akas/{aka}** – Search by alternative known-as titles (exact and case-sensitive).

### Actors

- **GET /actors** – Retrieve a list of actors with pagination.
- **GET /actors/{id}** – Get details about a specific actor.

### Utils

- **GET /title/utils/titleType** – Get available title types (e.g., movie, series).
- **GET /title/utils/genres** – Get a list of available genres.
- **GET /title/utils/lists** – Lists of predefined collections (e.g., top rated, most popular).

## Request and Response Format

### Request Example

For example, to fetch the most popular movies:

```http
GET /titles?list=most_pop_movies&limit=5&info=mini_info
