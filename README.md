# Handball API (Free)

The **Handball API** provides a comprehensive set of data for handball fans and developers, offering real-time updates, player statistics, team information, and more. This API is ideal for integrating detailed handball data into applications and services, enabling robust analysis and insights into the sport. This API is listed on [RAPIDAPI](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/handball-full-api)

## Key Features

- **Live Match Data**: Access real-time updates during handball matches, including scores, match events, and player performance.
- **Player Statistics**: Retrieve detailed statistics for handball players, including goals, assists, and defensive metrics.
- **Team Information**: Get information on handball teams, including rosters, rankings, and team performance metrics.
- **Match Schedules**: View upcoming matches, including dates, venues, and fixture details.
- **Historical Data**: Access past match results and player statistics for thorough analysis and historical comparisons.


## Getting Started

1. **Sign Up**: Create an account on RapidAPI.
2. **Subscribe**: Choose a subscription plan that fits your needs.
3. **API Key**: Obtain your unique API key to start making requests.
4. **Documentation**: For detailed usage instructions, visit the [Handball API Documentation](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/handball-full-api).



`For all these Leagues: EHFEL (MEN)
EHFEL (WOMEN)
EHFL, we have the listed endpoints`
## Endpoint: Retrieve Live Scores

### URL

`GET /live`

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing live scores data.

  ```json
  {
      "liveScores": [
          {
              "matchId": "12345",
              "teamA": "Team A",
              "teamB": "Team B",
              "scoreA": 12,
              "scoreB": 15,
              "status": "Live",
              "time": "15:00"
          },
          {
              "matchId": "12346",
              "teamA": "Team C",
              "teamB": "Team D",
              "scoreA": 20,
              "scoreB": 18,
              "status": "Live",
              "time": "16:00"
          }
          // more live scores
      ]
  }


## Endpoint: Retrieve News

### URL

`GET /news`

### Query Parameters

- `start` (number, optional): The starting index for news items. Default value is `0`.
- `limit` (number, optional): The maximum number of news items to return. Default value is `15`.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing news data based on the provided start index and limit.

  ```json
  {
      "news": [
          {
              "id": "1",
              "headline": "Team A Wins Championship",
              "date": "2024-07-23",
              "summary": "Team A clinched the championship title with a decisive victory over Team B."
          },
          {
              "id": "2",
              "headline": "Player X Transfers to New Team",
              "date": "2024-07-22",
              "summary": "Player X has signed with Team C after a successful season with Team D."
          }
          // more news items
      ]
  }


## Endpoint: Retrieve Live Tournament Information

### URL

`GET /live-tournament`

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing live tournament data.

  ```json
  {
      "liveTournaments": [
          {
              "tournamentId": "98765",
              "name": "Champions League",
              "status": "Ongoing",
              "matches": [
                  {
                      "matchId": "54321",
                      "teamA": "Team A",
                      "teamB": "Team B",
                      "scoreA": 1,
                      "scoreB": 2,
                      "time": "20:00"
                  },
                  {
                      "matchId": "54322",
                      "teamA": "Team C",
                      "teamB": "Team D",
                      "scoreA": 0,
                      "scoreB": 0,
                      "time": "22:00"
                  }
                  // more matches
              ]
          },
          {
              "tournamentId": "87654",
              "name": "World Cup",
              "status": "Ongoing",
              "matches": [
                  {
                      "matchId": "65432",
                      "teamA": "Team E",
                      "teamB": "Team F",
                      "scoreA": 2,
                      "scoreB": 3,
                      "time": "18:00"
                  }
                  // more matches
              ]
          }
          // more tournaments
      ]
  }


## Endpoint: Retrieve Live Matches

### URL

`GET /match`

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing live match data.

  ```json
  {
      "liveMatches": [
          {
              "matchId": "12345",
              "teamA": "Team A",
              "teamB": "Team B",
              "scoreA": 12,
              "scoreB": 15,
              "status": "Live",
              "time": "15:00",
              "tournament": "Champions League"
          },
          {
              "matchId": "12346",
              "teamA": "Team C",
              "teamB": "Team D",
              "scoreA": 20,
              "scoreB": 18,
              "status": "Live",
              "time": "16:00",
              "tournament": "World Cup"
          }
          // more live matches
      ]
  }


## Endpoint: Retrieve Live Match Detail

### URL

`GET /match-detail`

### Query Parameters

- `matchId` (string, required): The unique identifier of the match for which details are to be retrieved.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing detailed information about the specified match.

  ```json
  {
      "matchDetail": {
          "matchId": "202411020904002",
          "teamA": "Team A",
          "teamB": "Team B",
          "scoreA": 23,
          "scoreB": 20,
          "status": "In Progress",
          "time": "16:00",
          "tournament": "Champions League",
          "events": [
              {
                  "eventId": "1",
                  "type": "Try",
                  "team": "Team A",
                  "player": "Player X",
                  "minute": 12
              },
              {
                  "eventId": "2",
                  "type": "Penalty",
                  "team": "Team B",
                  "player": "Player Y",
                  "minute": 35
              }
              // more events
          ]
      }
  }



## Endpoint: Retrieve Top Scorer

### URL

`GET /top-scorer`

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing information about the top scorer.

  ```json
  {
      "topScorer": {
          "playerId": "12345",
          "playerName": "John Doe",
          "team": "Team A",
          "totalPoints": 150,
          "matchesPlayed": 20,
          "averagePointsPerMatch": 7.5
      }
  }


## Endpoint: Retrieve Standings

### URL

`GET /standings`

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing current standings.

  ```json
  {
      "standings": [
          {
              "teamId": "1",
              "teamName": "Team A",
              "points": 45,
              "wins": 15,
              "losses": 5,
              "draws": 2,
              "matchesPlayed": 22
          },
          {
              "teamId": "2",
              "teamName": "Team B",
              "points": 42,
              "wins": 14,
              "losses": 6,
              "draws": 2,
              "matchesPlayed": 22
          }
          // more teams
      ]
  }


## Endpoint: Retrieve Club Detail

### URL

`GET /club-detail`

### Query Parameters

- `clubId` (string, required): The unique identifier of the club for which details are to be retrieved.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing detailed information about the specified club.

  ```json
  {
      "clubDetail": {
          "clubId": "2yIVv2QUOdhAL-Qi0F_huw",
          "clubName": "Club Name",
          "founded": 1900,
          "stadium": "Stadium Name",
          "manager": "Manager Name",
          "league": "League Name",
          "location": "City, Country",
          "players": [
              {
                  "playerId": "123",
                  "playerName": "Player One",
                  "position": "Forward",
                  "nationality": "Country",
                  "age": 25
              },
              {
                  "playerId": "124",
                  "playerName": "Player Two",
                  "position": "Midfielder",
                  "nationality": "Country",
                  "age": 28
              }
              // more players
          ]
      }
  }


## Endpoint: Retrieve Player Detail

### URL

`GET /player-detail`

### Query Parameters

- `playerId` (string, required): The unique identifier of the player for whom details are to be retrieved.

### Responses

#### Success

- **Code**: 200 OK
- **Content**: JSON object containing detailed information about the specified player.

  ```json
  {
      "playerDetail": {
          "playerId": "joZjmClVXZLvJcS1OThzEg",
          "playerName": "Player Name",
          "position": "Position",
          "team": "Team Name",
          "nationality": "Country",
          "age": 25,
          "height": "6'0\"",
          "weight": "180 lbs",
          "stats": {
              "gamesPlayed": 50,
              "goals": 20,
              "assists": 15,
              "yellowCards": 3,
              "redCards": 1
          }
      }
  }


## Commonly Asked Questions

### 1. What kind of data can I access through the Handball API?
You can access live match data, player statistics, team information, match schedules, and historical data.

### 2. How do I authenticate my API requests?
You need to include your API key in the headers of your requests as specified in the API documentation.

### 3. Are there usage limits for the API?
Yes, usage limits depend on the subscription plan you select. Check the RapidAPI dashboard for details.

### 4. Can I filter data by specific matches, teams, or players?
Yes, the API allows filtering to retrieve data for specific matches, teams, or players.

### 5. Is historical data available for past matches?
Yes, the Handball API includes historical data for past matches, allowing for detailed analysis and comparisons.

### 6. How frequently is the data updated?
The data is updated in real-time during live matches and periodically for historical data and schedules.

### 7. Can I access data for both international and domestic handball leagues?
Yes, the API provides data for various international and domestic handball leagues and tournaments.

### 8. What formats does the API support for data responses?
The API supports data responses in JSON format, making it easy to integrate into various applications.

### 9. Are there specific endpoints for different types of data (e.g., scores, player stats)?
Yes, the API includes specific endpoints for various types of data, such as match scores, player statistics, and team information.

### 10. How can I stay updated on changes to the API?
You can stay informed about updates and changes by checking the API documentation and RapidAPI dashboard regularly.

For more information and to start using the Handball API, visit [Handball API on RapidAPI](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/handball-full-api).
