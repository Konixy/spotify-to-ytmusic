# Spotify to YouTube Music

Convert songs from **Spotify** to **YouTube Music**!

## Features

- Super **easy-to-use**
- **Audio only** results (no music videos)
- Convert **multiple songs**
- **99% accuracy**
- Perfect for **Discord Bots**
- Access/refresh token **not required**

## Installation

```bash
npm install spotify-to-ytmusic
```

## Usage

- To use **spotify-to-ytmusic**, first you need to provide your **[Spotify Credentials](https://www.avermedia.com/us/creator_central_spotify)**, in order to have access to the **Spotify API**.
- You can only provide **Tracks** *(Playlists, Albums and Podcasts are **NOT** supported!)*

## Example

### Import

- CommonJS

```javascript
const SpotifyToYoutubeMusic = require('spotify-to-ytmusic')
```

- ES6

```typescript
import SpotifyToYoutubeMusic from 'spotify-to-ytmusic';
```

### Usage

```javascript
// Set Spotify Credentials

const spotifyToYoutubeMusic = SpotifyToYoutubeMusic({
    clientID: "CLIENT_ID",
    clientSecret: "CLIENT_SECRET",
    accessToken: "ACCESS_TOKEN", // Optional
    ytMusicUrl: true // Optional
})

// Convert a Spotify Track

let song = await spotifyToYoutubeMusic('4cOdK2wGLETKBW3PvgPWqT')
console.log(song) // https://music.youtube.com/watch?v=lYBUbBu4W08
```

## Other ways to provide a Spotify Track

```javascript
await spotifyToYoutubeMusic('https://open.spotify.com/track/4cOdK2wGLETKBW3PvgPWqT')
```
```javascript
await spotifyToYoutubeMusic('spotify:track:4cOdK2wGLETKBW3PvgPWqT')
```
```javascript
await spotifyToYoutubeMusic('https://api.spotify.com/v1/tracks/4cOdK2wGLETKBW3PvgPWqT')
```
```javascript
await spotifyToYoutubeMusic('4cOdK2wGLETKBW3PvgPWqT')
```
```javascript
await spotifyToYoutubeMusic(['4cOdK2wGLETKBW3PvgPWqT','06JvOZ39sK8D8SqiqfaxDU'])
```

*This package is a TypeScript adaptation of [itsgox/spotify-to-ytmusic](https://github.com/itsgox/spotify-to-ytmusic)*
