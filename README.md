# UEFA Champions League

## Introduction

**UEFA Champions League API** provides comprehensive data from Europe's elite club football competition. This API provides detailed information through multiple endpoints including:

- **Standings**: Current group and knockout stage rankings.
- **Tables**: Group stage tables with points, goals, and match results.
- **Teams**: Detailed club information and statistics.
- **Players**: Individual player data and performance metrics.
- **Fixtures**: Upcoming matches and schedules.
- **Live Scores**: Real-time match results and updates.
- **Historical Data**: Past tournament records and statistics

Perfect for developers building sports apps, websites, or analysis tools focused on top-tier European football. Easily integrate Champions League data into your projects with our well-documented endpoints.

## Authentication

The URL you need to use is the following: `https://uefa-champions-league1.p.rapidapi.com/`
The API requires the headers listed below:

- **`x-rapidapi-host`**: `uefa-champions-league1.p.rapidapi.com`
- **`x-rapidapi-key`**: `YOUR_API_KEY`

Make sure to replace `YOUR_API_KEY` with your API key. You can register one [here](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/uefa-champions-league1/pricing).
Some frameworks automatically add extra headers, you have to make sure to remove them in order to get a response from the API.

## Caching

All endpoints use caching to improve performance.

## Endpoints

The API is configured to accept only **GET** requests. Below are the available endpoints with their descriptions and required parameters.

### 1. **`GET /athlete/bio`**

- **Description**: Retrieves biographical information for a specific player.

| Query Parameter | Type   | Default | Description                         | Required |
|-----------------|--------|---------|-------------------------------------|----------|
| `playerId`      | string | -       | The ID of the player                | Yes      |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/athlete/bio?playerId=150225', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "awards": {},
  "teamHistory": [
    {
      "id": "2572",
      "uid": "s:600~t:2572",
      "slug": "ita.como",
      "displayName": "Como",
      "logo": "https://a.espncdn.com/i/teamlogos/soccer/500/2572.png",
      "seasons": "2024-CURRENT",
      "links": [
        "https://www.espn.com/soccer/club/_/id/2572/como",
        "https://www.espn.com/soccer/team/stats/_/id/2572/como",
        "https://www.espn.com/soccer/team/fixtures/_/id/2572/como",
        "https://www.espn.com/soccer/team/results/_/id/2572/como",
        "https://www.espn.com/soccer/standings/_/league/ita.1",
        "https://www.espn.com/soccer/team/squad/_/id/2572/como"
      ],
      "seasonCount": "1",
      "isActive": true
    },
    {
      "id": "83",
      "uid": "s:600~t:83",
      "slug": "esp.barcelona",
      "displayName": "Barcelona",
      "logo": "https://a.espncdn.com/i/teamlogos/soccer/500/83.png",
      "seasons": "2010-2024",
      "links": [
        "https://www.espn.com/soccer/club/_/id/83/barcelona",
        ...
```

### 2. **`GET /athlete/overview`**

- **Description**: Retrieves an overview of a specific player.

| Query Parameter | Type   | Default | Description                         | Required |
|-----------------|--------|---------|-------------------------------------|----------|
| `playerId`      | string | -       | The ID of the player                | Yes      |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/athlete/overview?playerId=150225', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "statistics": {
    "labels": [
      "STRT",
      "FC",
      "FA",
      "YC",
      "RC",
      "G",
      "A",
      "SH",
      "ST",
      "OF"
    ],
    "names": [
      "starts",
      "foulsCommitted",
      "foulsSuffered",
      "yellowCards",
      "redCards",
      "totalGoals",
      "goalAssists",
      "totalShots",
      "shotsOnTarget",
      "offsides"
    ],
    "displayNames": [
      "Starts",
      "Fouls Committed",
      "Fouls Suffered",
      ...
```

### 3. **`GET /injuries`**

- **Description**: Retrieves injury information for the current season.

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/injuries', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "timestamp": "2024-10-31T17:45:28Z",
  "status": "success",
  "season": {
    "year": 2024,
    "type": 12885,
    "name": "League Phase",
    "displayName": "2024-25 UEFA Champions League"
  },
  "injuries": []
}
```

### 4. **`GET /standingsv2`**

- **Description**: Retrieves standings for a specific season.

| Query Parameter | Type   | Default | Description                         | Required |
|-----------------|--------|---------|-------------------------------------|----------|
| `season`        | string | `2023`  | The year of the season (YYYY)       | No       |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/standingsv2?season=2024', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "uid": "s:600~l:775",
  "id": "2",
  "name": "UEFA Champions League",
  "abbreviation": "UEFA Champions League",
  "children": [
    {
      "uid": "s:600~l:775~g:1",
      "id": "1",
      "name": "League Phase",
      "abbreviation": "2024-25",
      "standings": {
        "id": "0",
        "name": "overall",
        "displayName": "Overall Standings",
        "links": [
          {
            "language": "en-US",
            "rel": [
              "standings",
              "desktop"
            ],
            "href": "https://www.espn.com/soccer/table/_/league/uefa.champions",
            "text": "Full Table",
            "shortText": "Standings",
            "isExternal": false,
            "isPremium": false
          }
        ],
        "season": 2024,
        ...
```

### 5. **`GET /athlete/statistic`**

- **Description**: Retrieves detailed statistics for a specific player.

| Query Parameter | Type   | Default | Description                         | Required |
|-----------------|--------|---------|-------------------------------------|----------|
| `playerId`      | string | -       | The ID of the player                | Yes      |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/athlete/statistic?playerId=150225', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "id": "0",
  "name": "Total",
  "abbreviation": "Total",
  "type": "total",
  "categories": [
    {
      "name": "defensive",
      "displayName": "Defensive",
      "shortDisplayName": "Defensive",
      "abbreviation": "def",
      "summary": "",
      "stats": [
        {
          "name": "blockedShots",
          "displayName": "Shots Blocked",
          "shortDisplayName": "SHBLK",
          "description": "The number shots blocked by a defender.",
          "abbreviation": "SHBLK",
          "value": 2,
          "displayValue": "2"
        },
        {
          "name": "effectiveClearance",
          "displayName": "Effective Clearance",
          "shortDisplayName": "EFFCL",
          "description": "The number of clearances that stops the attack of the opposing team.",
          "abbreviation": "EFFCL",
          "value": 33,
          "displayValue": "33"
          ...
```

### 6. **`GET /athlete/leagues`**

- **Description**: Retrieves leagues information for a specific player.

| Query Parameter | Type   | Default | Description                         | Required |
|-----------------|--------|---------|-------------------------------------|----------|
| `playerId`      | string | -       | The ID of the player                | Yes      |
| `page`          | string | `1`     | The page number for pagination      | No       |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/athlete/leagues?playerId=150225', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "count": 21,
  "pageIndex": 1,
  "pageSize": 25,
  "pageCount": 1,
  "availableSeasons": [
    "ita 1",
    "ita coppa italia",
    "esp super cup",
    "esp joan gamper",
    "uefa champions",
    "esp 1",
    "esp copa del rey",
    "club friendly",
    "uefa europa",
    "fifa worldq uefa",
    "uefa nations",
    "uefa super cup",
    "fifa friendly",
    "uefa euroq",
    "global champs cup",
    "fifa world",
    "uefa euro",
    "fifa cwc",
    "uefa euro u21",
    "esp 2",
    "fifa world u20"
  ]
}
```

### 7. **`GET /athlete/season`**

- **Description**: Retrieves season statistics for a specific player.

| Query Parameter | Type   | Default | Description                         | Required |
|-----------------|--------|---------|-------------------------------------|----------|
| `playerId`      | string | -       | The ID of the player                | Yes      |
| `page`          | string | `1`     | The page number for pagination      | No       |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/athlete/season?playerId=150225', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "count": 18,
  "pageIndex": 1,
  "pageSize": 25,
  "pageCount": 1,
  "availableSeasons": [
      "2023",
      "2022",
      "2021",
      "2020",
      "2019",
      "2018",
      "2017",
      "2016",
      "2015",
      "2014",
      "2013",
      "2012",
      "2011",
      "2010",
      "2009",
      "2008",
      "2007",
      "2006"
  ]
}
```

### 8. **`GET /news`**

- **Description**: Retrieves the latest news.

| Query Parameter | Type   | Default | Description                                | Required |
|-----------------|--------|---------|--------------------------------------------|----------|
| `limit`         | string | `23`    | The maximum number of news items to return | Yes      |

Example request:

```javascript
fetch('', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
[
  {
    "description": "Former Liverpool manager Jürgen Klopp has taken a swipe at Sergio Ramos when discussing the ex-Real Madrid star on a podcast with Toni Kroos.",
    "headline": "Jürgen Klopp questions if Sergio Ramos is a 'good guy'",
    "images": [
      "https://a.espncdn.com/photo/2023/1019/r1240588_1296x729_16-9.jpg"
    ],
    "link": "https://www.espn.com/soccer/story/_/id/42108171/jurgen-klopp-questions-sergio-ramos-good-guy",
    "published": "2024-10-31T16:36:24Z",
    "premium": false,
    "lastModified": "2024-10-31T16:36:21Z",
    "category": {
      "id": 142295,
      "description": "Liverpool - ENG.LIVERPOOL",
      "type": "team",
      "sportId": 600,
      "leagueId": "",
      "createDate": "2024-10-31T10:15:00Z"
    }
  },
  {
    "description": "Jan Åge Fjørtoft speaks about Manchester United's links with Sporting CP manager Rúben Amorim.",
    "headline": "Why Rúben Amorim would need to start winning 'straight away' at Man United",
    "images": [
      "https://a.espncdn.com/media/motion/2024/1030/dm_241030_COM_SOC_Analysis_Why_Ruben_Amorim_would_need_to_start_winning_straight_away_at_Man_United_202410/dm_241030_COM_SOC_Analysis_Why_Ruben_Amorim_would_need_to_start_winning_straight_away_at_Man_United_202410.jpg"
    ],
    "link": "https://www.espn.com/video/clip?id=42087437",
    "published": "2024-10-30T09:49:08Z",
    "premium": false,
    "lastModified": "2024-10-30T09:49:02Z",
    ...
```

### 9. **`GET /standings`**

- **Description**: Retrieves standings for a specific year and group type.

| Query Parameter | Type   | Default  | Description                                     | Required |
|-----------------|--------|----------|-------------------------------------------------|----------|
| `year`          | string | -        | The year of the standings (YYYY)                | Yes      |
| `group`         | string | `league` | The group type (league, conference or division) | No       |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/standings?year=2022', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "standings": {
    "uid": "s:600~l:775",
    "id": "8675309",
    "name": "UEFA Champions League",
    "abbreviation": "UEFA Champions League",
    "seasons": [
      {
        "year": 2024,
        "startDate": "2024-07-01T04:00Z",
        "endDate": "2025-07-01T03:59Z",
        "displayName": "2024-25 UEFA Champions League",
        "types": [
          {
            "id": "1",
            "name": "League Phase",
            "abbreviation": "League Phase",
            "startDate": "2024-08-29T04:00Z",
            "endDate": "2025-01-31T04:59Z",
            "hasStandings": true
          },
          {
            "id": "2",
            "name": "Knockout Round Playoffs",
            "abbreviation": "Knockout Round Playoffs",
            "startDate": "2025-01-31T05:00Z",
            "endDate": "2025-02-21T04:59Z",
            "hasStandings": false
          },
          {
            ...
```

### 10. **`GET /scoreboard`**

- **Description**: Retrieves the scoreboard for a specific date.

| Query Parameter | Type   | Default | Description                             | Required |
|-----------------|--------|---------|-----------------------------------------|----------|
| `year`          | string | -       | The year of the scoreboard (YYYY)       | Yes      |
| `month`         | string | -       | The month of the scoreboard (MM)        | No       |
| `day`           | string | -       | The day of the scoreboard (DD)          | No       |
| `limit`         | string | `100`   | The maximum number of results           | No       |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/scoreboard?year=2023', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "scoreboard": {
    "leagues": [
      {
        "id": "775",
        "uid": "s:600~l:775",
        "name": "UEFA Champions League",
        "abbreviation": "UEFA Champions League",
        "midsizeName": "UEFA.CHAMPIONS",
        "slug": "uefa.champions",
        "season": {
          "year": 2023,
          "startDate": "2023-08-24T04:00Z",
          "endDate": "2024-07-01T03:59Z",
          "displayName": "2023-24 UEFA Champions League",
          "type": {
            "id": "5",
            "type": 12082,
            "name": "Final",
            "abbreviation": "Final"
          }
        },
        "logos": [
          {
            "href": "https://a.espncdn.com/i/leaguelogos/soccer/500/2.png",
            "width": 500,
            "height": 500,
            "alt": "",
            "rel": [
              "full",
              ...
```

### 11. **`GET /schedule`**

- **Description**: Retrieves the schedule for a specific date or year.

| Query Parameter | Type   | Default | Description                           | Required |
|-----------------|--------|---------|---------------------------------------|----------|
| `year`          | string | -       | The year of the schedule (YYYY)       | Yes      |
| `month`         | string | -       | The month of the schedule (MM)        | No       |
| `day`           | string | -       | The day of the schedule (DD)          | No       |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/schedule?year=2023', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "schedule": {
    "20221231": [],
    "20230101": [
      {
        "id": "656857",
        "competitors": [
          {
            "id": "367",
            "abbrev": "TOT",
            "displayName": "Tottenham Hotspur",
            "shortDisplayName": "Tottenham Hotspur",
            "logo": "https://a.espncdn.com/i/teamlogos/soccer/500/367.png",
            "teamColor": "ffffff",
            "altColor": "9bafd8",
            "uid": "s:600~t:367",
            "recordSummary": "",
            "standingSummary": "",
            "location": "Tottenham Hotspur",
            "links": "/soccer/team/_/id/367/tottenham-hotspur",
            "name": "Tottenham Hotspur",
            "shortName": "Tottenham",
            "isHome": false,
            "score": 0
          },
          {
            "id": "103",
            "abbrev": "MIL",
            "displayName": "AC Milan",
            "shortDisplayName": "AC Milan",
            ...
```

### 12. **`GET /summary`**

- **Description**: Retrieves the summary for a specific game.

| Query Parameter | Type   | Default | Description                         | Required |
|-----------------|--------|---------|-------------------------------------|----------|
| `gameId`        | string | -       | The ID of the game                  | Yes      |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/summary?gameId=702410', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "boxScore": {
    "form": [
      {
        "displayOrder": 1,
        "team": {
          "id": "124",
          "uid": "s:600~t:124",
          "displayName": "Borussia Dortmund",
          "abbreviation": "DOR",
          "links": [
            {
              "href": "https://www.espn.com/soccer/club/_/id/124/borussia-dortmund",
              "text": "Clubhouse"
            },
            {
              "href": "https://www.espn.com/soccer/team/fixtures/_/id/124/borussia-dortmund",
              "text": "Fixtures"
            }
          ],
          "logo": "https://a.espncdn.com/i/teamlogos/soccer/500/124.png",
          "logos": [
            {
              "href": "https://a.espncdn.com/i/teamlogos/soccer/500/124.png",
              "width": 500,
              "height": 500,
              "alt": "",
              "rel": [
                "full",
                "default"
                ...
```

### 13. **`GET /boxscore`**

- **Description**: Retrieves the box score for a specific game.

| Query Parameter | Type   | Default | Description                         | Required |
|-----------------|--------|---------|-------------------------------------|----------|
| `gameId`        | string | -       | The ID of the game                  | Yes      |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/boxscore?gameId=702410', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "boxscore": {
    "form": [
      {
        "displayOrder": 1,
        "team": {
          "id": "124",
          "uid": "s:600~t:124",
          "displayName": "Borussia Dortmund",
          "abbreviation": "DOR",
          "links": [
            {
              "href": "https://www.espn.com/soccer/club/_/id/124/borussia-dortmund",
              "text": "Clubhouse"
            },
            {
              "href": "https://www.espn.com/soccer/team/fixtures/_/id/124/borussia-dortmund",
              "text": "Fixtures"
            }
          ],
          "logo": "https://a.espncdn.com/i/teamlogos/soccer/500/124.png",
          "logos": [
            {
              "href": "https://a.espncdn.com/i/teamlogos/soccer/500/124.png",
              "width": 500,
              "height": 500,
              "alt": "",
              "rel": [
                "full",
                "default"
                ...
```

### 14. **`GET /team/roster`**

- **Description**: Retrieves the roster for a specific team.

| Query Parameter | Type   | Default | Description                         | Required |
|-----------------|--------|---------|-------------------------------------|----------|
| `teamId`        | string | -       | The ID of the team                  | Yes      |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/team/roster?teamId=83', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "status": "success",
  "season": {
    "year": 2024,
    "displayName": "2024-25 UEFA Champions League",
    "type": 12885,
    "name": "League Phase"
  },
  "athletes": [
    {
      "id": "140740",
      "uid": "s:600~a:140740",
      "guid": "82c738d7-e78c-30d5-9d87-ff758417f2bd",
      "firstName": "Marc-André",
      "lastName": "ter Stegen",
      "fullName": "Marc-André ter Stegen",
      "displayName": "Marc-André ter Stegen",
      "shortName": "M ter Stegen",
      "weight": 185,
      "displayWeight": "185 lbs",
      "height": 74,
      "displayHeight": "6' 2\"",
      "age": 32,
      "dateOfBirth": "1992-04-30T07:00Z",
      "birthPlace": {
        "country": "Germany"
      },
      "citizenship": "Germany",
      "gender": "MALE",
      "citizenshipCountry": {
        ...
```

### 15. **`GET /team/info`**

- **Description**: Retrieves information about a specific team.

| Query Parameter | Type   | Default | Description                         | Required |
|-----------------|--------|---------|-------------------------------------|----------|
| `teamId`        | string | -       | The ID of the team                  | Yes      |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/team/info?teamId=83', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "id": "83",
  "uid": "s:600~t:83",
  "slug": "esp.barcelona",
  "location": "Barcelona",
  "name": "Barcelona",
  "abbreviation": "BAR",
  "displayName": "Barcelona",
  "shortDisplayName": "Barcelona",
  "color": "00529f",
  "alternateColor": "2f2f2f",
  "isActive": true,
  "logos": [
    "https://a.espncdn.com/i/teamlogos/soccer/500/83.png",
    "https://a.espncdn.com/i/teamlogos/soccer/500-dark/83.png"
  ],
  "record": {
    "items": [
      {
        "description": "Overall Record",
        "type": "total",
        "summary": "2-0-1",
        "stats": [
          {
            "name": "gamesPlayed",
            "value": 3
          },
          {
            "name": "losses",
            "value": 1
            ...
```

### 16. **`GET /team/list`**

- **Description**: Retrieves a list of teams.

| Query Parameter | Type   | Default | Description                           | Required |
|-----------------|--------|---------|---------------------------------------|----------|
| `limit`         | string | `400`   | The maximum number of teams to return | No       |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/team/list?limit=45', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
[
  {
    "id": "103",
    "uid": "s:600~t:103",
    "slug": "ita.ac_milan",
    "abbreviation": "MIL",
    "displayName": "AC Milan",
    "shortDisplayName": "Milan",
    "name": "AC Milan",
    "location": "AC Milan",
    "color": "e4002b",
    "alternateColor": "ffffff",
    "isActive": true,
    "isAllStar": false,
    "logos": [
      "https://a.espncdn.com/i/teamlogos/soccer/500/103.png",
      "https://a.espncdn.com/i/teamlogos/soccer/500-dark/103.png"
    ],
    "links": [
      "https://www.espn.com/soccer/club/_/id/103/ac-milan",
      "https://www.espn.com/soccer/team/stats/_/id/103/ac-milan",
      "https://www.espn.com/soccer/team/fixtures/_/id/103/ac-milan"
    ]
  },
  {
    "id": "174",
    "uid": "s:600~t:174",
    "slug": "fra.monaco",
    "abbreviation": "MON",
    "displayName": "AS Monaco",
    ...
```

### 17. **`GET /team/statistic/discipline`**

- **Description**: Retrieves discipline statistics for a specific team.

| Query Parameter | Type   | Default | Description                         | Required |
|-----------------|--------|---------|-------------------------------------|----------|
| `teamId`        | string | -       | The ID of the team                  | Yes      |
| `season`        | string | `2023`  | The year of the season (YYYY)       | No       |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/team/statistic/discipline?teamId=83', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "status": "success",
  "requestedSeason": {
    "year": 2023,
    "type": 12082,
    "name": "Final",
    "displayName": "2023-24 UEFA Champions League"
  },
  "results": [
    {
      "id": "323702",
      "uid": "s:600~a:323702",
      "guid": "3ea1fd25-9cb7-362b-bc0c-e75dcd5705de",
      "displayName": "Gavi",
      "shortName": "Gavi",
      "links": [
        "https://www.espn.com/soccer/player/_/id/323702/gavi",
        "https://www.espn.com/soccer/player/stats/_/id/323702/gavi",
        "https://www.espn.com/soccer/player/splits/_/id/323702/gavi",
        "https://www.espn.com/soccer/player/matches/_/id/323702/gavi",
        "https://www.espn.com/soccer/player/news/_/id/323702/gavi",
        "https://www.espn.com/soccer/player/bio/_/id/323702/gavi",
        "https://www.espn.com/soccer/player/_/id/323702/gavi",
        "https://www.espn.com/soccer/player/transfers/_/id/323702/gavi",
        "https://www.espn.com/soccer/player/transfers/_/id/323702/gavi"
      ],
      "jersey": "6",
      "statistics": [
        {
          "name": "appearances",
          ...
```

### 18. **`GET /team/statistic/scoring`**

- **Description**: Retrieves scoring statistics for a specific team.

| Query Parameter | Type   | Default | Description                         | Required |
|-----------------|--------|---------|-------------------------------------|----------|
| `teamId`        | string | -       | The ID of the team                  | Yes      |
| `season`        | string | `2023`  | The year of the season (YYYY)       | No       |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/team/statistic/scoring?teamId=83', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "status": "success",
  "requestedSeason": {
    "year": 2023,
    "type": 12082,
    "name": "Final",
    "displayName": "2023-24 UEFA Champions League"
  },
  "results": {
    "stats": [
      {
        "name": "goalsLeaders",
        "displayName": "Goals",
        "shortDisplayName": "Goals",
        "abbreviation": "G",
        "leaders": [
          {
            "displayValue": "Matches: 9, Goals: 3",
            "shortDisplayValue": "M: 9, G: 3: A: 1",
            "value": 3,
            "athlete": {
              "id": "125824",
              "uid": "s:600~a:125824",
              "guid": "df6ff39c-5f60-ac23-937e-c293506e78bf",
              "displayName": "Robert Lewandowski",
              "shortName": "R Lewandowski",
              "links": [
                {
                  "language": "en-US",
                  "rel": [
                    ...
```

### 19. **`GET /team/perfomance`**

- **Description**: Retrieves performance data for a specific team.

| Query Parameter | Type   | Default | Description                         | Required |
|-----------------|--------|---------|-------------------------------------|----------|
| `teamId`        | string | -       | The ID of the team                  | Yes      |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/team/perfomance?teamId=83', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "status": "success",
  "results": {
    "stats": {
      "performance": [
        {
          "name": "mostHomeGoalsGameId",
          "displayName": "Goals Scored (H)",
          "shortDisplayName": "Goals Scored (H)",
          "description": "The game with most goals scored at home",
          "abbreviation": "GSH",
          "competition": {
            "date": "2024-10-01T19:00Z",
            "attendance": 45097,
            "competitors": [
              {
                "homeAway": "home",
                "winner": true,
                "team": {
                  "id": "83",
                  "uid": "s:600~t:83",
                  "name": "Barcelona",
                  "abbreviation": "BAR",
                  "displayName": "Barcelona",
                  "shortDisplayName": "Barcelona",
                  "logos": [
                    {
                      "href": "https://a.espncdn.com/i/teamlogos/soccer/500/83.png",
                      "width": 500,
                      "height": 500,
                      ...
```

### 20. **`GET /team/transfers`**

- **Description**: Retrieves transfer information for a specific team.

| Query Parameter | Type   | Default | Description                               | Required |
|-----------------|--------|---------|-------------------------------------------|----------|
| `teamId`        | string | -       | The ID of the team                        | Yes      |
| `season`        | string | `2023`  | The year of the season (YYY)              | No       |
| `limit`         | string | `100`   | The maximum number of transfers to return | No       |
| `page`          | string | `1`     | The page number for pagination            | No       |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/team/transfers?teamId=83', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "timestamp": "2024-10-31T18:23:04Z",
  "status": "success",
  "count": 32,
  "pageIndex": 1,
  "pageSize": 100,
  "pageCount": 1,
  "requestedYear": {
    "year": 2023,
    "displayName": "2023"
  },
  "transactions": {
    "in": [
      {
        "date": "2023-09-01T07:00Z",
        "athlete": {
          "id": "176399",
          "firstName": "João",
          "lastName": "Cancelo",
          "displayName": "João Cancelo",
          "links": [
            "https://www.espn.com/soccer/player/_/id/176399/joao-cancelo",
            "https://www.espn.com/soccer/player/stats/_/id/176399/joao-cancelo",
            "https://www.espn.com/soccer/player/splits/_/id/176399/joao-cancelo",
            "https://www.espn.com/soccer/player/matches/_/id/176399/joao-cancelo",
            "https://www.espn.com/soccer/player/news/_/id/176399/joao-cancelo",
            "https://www.espn.com/soccer/player/bio/_/id/176399/joao-cancelo",
            "https://www.espn.com/soccer/player/_/id/176399/joao-cancelo",
            "https://www.espn.com/soccer/player/transfers/_/id/176399/joao-cancelo",
            "https://www.espn.com/soccer/player/transfers/_/id/176399/joao-cancelo"
            ...
```

### 21. **`GET /team/results`**

- **Description**: Retrieves results for a specific team in a given season.

| Query Parameter | Type   | Default | Description                         | Required |
|-----------------|--------|---------|-------------------------------------|----------|
| `teamId`        | string | -       | The ID of the team                  | Yes      |
| `season`        | string | -       | The year of the season (YYYY)       | Yes      |

Example request:

```javascript
fetch('https://uefa-champions-league1.p.rapidapi.com/team/results?teamId=83&season=2023', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'uefa-champions-league1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "status": "success",
  "requestedSeason": {
    "year": 2023,
    "type": 12084,
    "name": "Quarterfinals",
    "displayName": "2023-24 UEFA Champions League"
  },
  "events": [
    {
      "id": "700723",
      "date": "2024-04-16T19:00Z",
      "name": "Paris Saint-Germain at Barcelona",
      "shortName": "PSG @ BAR",
      "season": {
        "year": 2023,
        "displayName": "2023-24 UEFA Champions League"
      },
      "seasonType": {
        "id": "3",
        "type": 12084,
        "name": "Quarterfinals",
        "abbreviation": "Quarterfinals"
      },
      "timeValid": true,
      "competitions": {
        "id": "700723",
        "date": "2024-04-16T19:00Z",
        "attendance": 50309,
        "timeValid": true,
        ...
```

## Error Handling

The  API returns standard HTTP status codes to indicate the success or failure of API requests. Below are common errors and suggestions for handling them.

|Status Code|Message|Description|Suggested Handling|
|--|--|--|--|
| **400** | Bad Request | The request was malformed or missing required parameters (e.g., `domain` parameter not provided). | Verify that all required parameters are included and correctly formatted. |
| **401** | Unauthorized | Invalid or missing API key in the request headers. | Check that a valid API key is included in `x-rapidapi-key`. |
| **403** | Forbidden | Access to the requested resource is denied, possibly due to rate limits or restricted access. | Review rate limits and ensure API permissions. Retry after a delay if rate limit exceeded. |
| **404** | Not Found | The requested domain information could not be found (e.g., domain does not exist). | Check the spelling or availability of the domain. |
| **429** | Too Many Requests | The API rate limit has been exceeded. | Implement rate-limiting logic and retry after the specified rate limit reset time. |
| **500** | Internal Server Error | A server error occurred while processing the request. | Retry the request after a few seconds. If the error persists, contact API support. |
| **503** | Service Unavailable | The API service is temporarily unavailable (e.g., due to maintenance). | Retry the request later or check the API status page for maintenance alerts. |
