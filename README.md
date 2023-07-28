# papercliff

Papercliff looks at the world’s largest news agencies, reads articles, identifies and shares keywords. To use this API, visit the following webpage and get an X-RapidAPI-Key:

https://rapidapi.com/dimos86m/api/papercliff/

## Endpoints


--------



### 1. Popular Keywords


Returns the 100 most popular keywords with the corresponding number of news agencies and articles from which they have been cited.



***Endpoint:***

```bash
Method: GET
URL: https://papercliff.p.rapidapi.com/keywords
```


***Headers:***

| Key | Value |
| --- | ------|
| Accept | application/json |
| X-RapidAPI-Host | papercliff.p.rapidapi.com |
| X-RapidAPI-Key | XXXXXXXXXXXXXXX |



***Query params:***

| Key | Description                                                                                                                                                                                                        |
| --- |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| from | Narrows down the results to articles published after the provided date-time in UTC. The format should be `yyyy-MM-dd'T'HH:mm` (example `2022-09-18T13:45`). Date-times older than a week do not affect the result. |
| to | Narrows down the results to articles published before the provided date-time in UTC. The format should be `yyyy-MM-dd'T'HH:mm` (example `2022-09-18T15:30`). Date-times of the future do not affect the result.    |
| terms | Narrows down the results to articles that contain all the provided keywords. The terms should consist of one to three words separated by a dash (example `election-campaign`).                                     |
| offset | Omits a number of keywords.                                                                                                                                                                                        |


#### Example Response
```js
[
    {
        "keyword": "iran",
        "articles": 398,
        "agencies": 37
    },
    {
        "keyword": "ukraine",
        "articles": 2001,
        "agencies": 36
    },
    {
        "keyword": "russia",
        "articles": 1582,
        "agencies": 36
    },
    {
        "keyword": "russian",
        "articles": 729,
        "agencies": 36
    },
    {
        "keyword": "hurricane",
        "articles": 914,
        "agencies": 35
    },
    ...
]
```



### 2. Recent Articles


Returns the 100 most recent articles and their keywords.



***Endpoint:***

```bash
Method: GET
URL: https://papercliff.p.rapidapi.com/timeline
```


***Headers:***

| Key | Value |
| --- | ------|
| Accept | application/json |
| X-RapidAPI-Host | papercliff.p.rapidapi.com |
| X-RapidAPI-Key | XXXXXXXXXXXXXXX |



***Query params:***

| Key | Description                                                                                                                                                                                                        |
| --- |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| from | Narrows down the results to articles published after the provided date-time in UTC. The format should be `yyyy-MM-dd'T'HH:mm` (example `2022-09-18T13:45`). Date-times older than a week do not affect the result. |
| to | Narrows down the results to articles published before the provided date-time in UTC. The format should be `yyyy-MM-dd'T'HH:mm` (example `2022-09-18T15:30`). Date-times of the future do not affect the result.    |
| terms | Narrows down the results to articles that contain all the provided keywords. The terms should consist of one to three words separated by a dash (example `election-campaign`).                                     |
| offset | Omits a number of articles.                                                                                                                                                                                        |


#### Example Response
```js
[
    {
        "datetime": "2022-10-01T16:14",
        "story": "coast-hurricane-mexico-orlene-strengthens"
    },
    {
        "datetime": "2022-10-01T16:13",
        "story": "danes-leaking-nord-pipeline-stream"
    },
    {
        "datetime": "2022-10-01T16:13",
        "story": "border-lebanon-maritime-proposal"
    },
    {
        "datetime": "2022-10-01T16:12",
        "story": "decades-rose-seen-strathmore-tiara"
    },
    {
        "datetime": "2022-10-01T16:12",
        "story": "abbie-birth-burnett-david-duggar"
    },
    ...
]
```



### 3. Popular Combinations


Returns the 100 most popular combinations/triples of keywords with the corresponding number of news agencies and articles from which they have been cited.



***Endpoint:***

```bash
Method: GET
URL: https://papercliff.p.rapidapi.com/combinations
```


***Headers:***

| Key | Value |
| --- | ------|
| Accept | application/json |
| X-RapidAPI-Host | papercliff.p.rapidapi.com |
| X-RapidAPI-Key | XXXXXXXXXXXXXXX |



***Query params:***

| Key | Description                                                                                                                                                                                                        |
| --- |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| from | Narrows down the results to articles published after the provided date-time in UTC. The format should be `yyyy-MM-dd'T'HH:mm` (example `2022-09-18T13:45`). Date-times older than a week do not affect the result. |
| to | Narrows down the results to articles published before the provided date-time in UTC. The format should be `yyyy-MM-dd'T'HH:mm` (example `2022-09-18T15:30`). Date-times of the future do not affect the result.    |
| terms | Narrows down the results to articles that contain all the provided keywords. The terms should consist of one to three words separated by a dash (example `election-campaign`).                                     |
| offset | Omits a number of combinations.                                                                                                                                                                                    |


#### Example Response
```js
[
    {
        "story": "giorgia-italy-meloni",
        "articles": 85,
        "agencies": 24
    },
    {
        "story": "florida-hurricane-ian",
        "articles": 135,
        "agencies": 23
    },
    {
        "story": "citizenship-russian-snowden",
        "articles": 47,
        "agencies": 22
    },
    {
        "story": "abe-funeral-japan",
        "articles": 49,
        "agencies": 21
    },
    {
        "story": "citizenship-putin-snowden",
        "articles": 47,
        "agencies": 20
    },
    ...
]
```



### 4. Articles per Day


Returns the number of articles published daily during the last week and the number of corresponding news agencies that created those articles.



***Endpoint:***

```bash
Method: GET
URL: https://papercliff.p.rapidapi.com/history
```


***Headers:***

| Key | Value |
| --- | ------|
| Accept | application/json |
| X-RapidAPI-Host | papercliff.p.rapidapi.com |
| X-RapidAPI-Key | XXXXXXXXXXXXXXX |



***Query params:***

| Key | Description |
| --- |-------------|
| terms | Narrows down the results to articles that contain all the provided keywords. The terms should consist of one to three words separated by a dash (example `election-campaign`). |


#### Example Response
```js
[
    {
        "day": "2022-10-01",
        "articles": 1366,
        "agencies": 50
    },
    {
        "day": "2022-09-30",
        "articles": 3166,
        "agencies": 64
    },
    {
        "day": "2022-09-29",
        "articles": 3138,
        "agencies": 62
    },
    {
        "day": "2022-09-28",
        "articles": 3036,
        "agencies": 57
    },
    {
        "day": "2022-09-27",
        "articles": 3096,
        "agencies": 61
    },
    {
        "day": "2022-09-26",
        "articles": 3091,
        "agencies": 65
    },
    {
        "day": "2022-09-25",
        "articles": 1906,
        "agencies": 53
    },
    {
        "day": "2022-09-24",
        "articles": 1881,
        "agencies": 53
    }
]
```



### 5. Summary Statistics


Returns summary statistics about how many keywords have been found and how many articles and agencies papercliff looked at.



***Endpoint:***

```bash
Method: GET
URL: https://papercliff.p.rapidapi.com/overview
```


***Headers:***

| Key | Value |
| --- | ------|
| Accept | application/json |
| X-RapidAPI-Host | papercliff.p.rapidapi.com |
| X-RapidAPI-Key | XXXXXXXXXXXXXXX |



***Query params:***

| Key | Description |
| --- |-------------|
| from | Narrows down the results to articles published after the provided date-time in UTC. The format should be `yyyy-MM-dd'T'HH:mm` (example `2022-09-18T13:45`). Date-times older than a week do not affect the result. |
| to | Narrows down the results to articles published before the provided date-time in UTC. The format should be `yyyy-MM-dd'T'HH:mm` (example `2022-09-18T15:30`). Date-times of the future do not affect the result. |
| terms | Narrows down the results to articles that contain all the provided keywords. The terms should consist of one to three words separated by a dash (example `election-campaign`). |


#### Example Response
```js
{
    "articles": 20673,
    "agencies": 73,
    "findings": 99926,
    "keywords": 16280
}
```
