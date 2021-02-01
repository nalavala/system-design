# Spotify Clone

This is my perspective of designing spotify

## Functional Scope
1. All curd operations for songs/albums.
2. fetching top 10 trending songs based on language.
3. Fetching top 10 songs for users.
4. Fetching top 50 releasing songs based on language.

## Estimations


## List of services and functionalities
1. Songs service

    This service is responsiable to perform all the curd operations related to songs.
2. Trending Service

    This service is responsiable to fetch all trending songs based on different context like languages,time(year,month),users etc. This service is prepare the data beforehand to avoid latency while fetching trending songs. This listens to the events emited by songs service like view,upload etc. It prepares the data based on the events for fast retrival.


## Data models


## List of API's
