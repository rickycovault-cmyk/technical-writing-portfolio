# API Documentation

## GET /getHeartRate

### Description
Returns the user's current heart rate.

### Parameters
- userId (string) - required

### Example Request
GET /getHeartRate?userId=12345

### Example Response
{"heartRate": 81, "unit": "bpm"}


## GET /getSongMatch

### Description 
Returns a list of 10 different songs matching the user's current heart rate. 

### Parameters
- userId (string) - required
- bpm (number) - required
- limit (number) - optional

### Example Request
GET /getSongMatch?userId=12345&bpm=80&limit=10

### Example Response
{
  "songs": [
    { "title": "Song 1", "artist": "Artist A", "bpm": 80 },
    { "title": "Song 2", "artist": "Artist B", "bpm": 80 }
  ]
}


## GET /connectMusic

### Description 
Connect a user's preferred music account. 

### Parameters
- userId (string) - required
- provider (string) - required (e.g., Spotify)

### Example Request
GET /connectMusic?userId=12345&provider=spotify

### Example Response
{"status": "connected", "provider": "spotify"} 