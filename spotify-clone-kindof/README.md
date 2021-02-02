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
2. Trending Service


## Data models

## Data models for song service

## song-metadata
```JSON
{
    "id" : "string",
    "name" : "string",
    "length" : "Integer",
    "album" : "<album Id>",
    "artist" : "<artist-Id>",
    "singers" : ["<singer Id>"],
    "contentLanguage" : "EN",
    "streamURL" : "<URL>",
    "image" : "<url ofimage thumbnail>",
    "format" : "mp3",
    "publisher" : "Publisher-id",
    "createdAt" : "Date"
}
```
## user
```JSON
{
    "id" : "String",
    "username" : "string",
    "email" : "email",
    "password" : "password"
}
````
## Data models for Trending Service

## song-listen-count
```JSON
{
    "songId" : "id of the song",
    "listenCount" : "Integer"
}
````
## user-listen-count
```JSON
{
    "userId" : "id of the user",
    "songId" : "id of the song",
    "listenCount" : "Integer"
}
````
## trending-songs-language
```JSON
{
    "id" : "id of the user",
    "language" : "EN",
    "songs" : ["songId", "songId"]
}
````
## trending-songs-user
```JSON
{
    "id" : "id of the user",
    "userId" : "userId",
    "songs" : ["songId", "songId"]
}
````
## trending-songs-release
```JSON
{
    "id" : "id of the user",
    "language" : "EN",
    "songs" : ["songId", "songId"]
}
````

## List of API's
