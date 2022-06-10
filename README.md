# Spotify to YouTube Music

Convert songs from **Spotify** to **YouTube Music**!

## Changelog

> - The authentication is now handled by **spotify-to-ytmusic**, only using a **Client ID** & **Client Secret**, the previously required **Redirect URI** & **Access Token** are not needed anymore.
> - **spotify-to-ytmusic** is now much faster.
> - The **YouTube Music** results are now much more accurate.

## Installation

```bash
npm install spotify-to-ytmusic
```

## Usage

- To use **Spotify to YouTube Music**, first you need to provide your **Spotify Credentials** (**[Client ID & Client Secret](https://www.avermedia.com/us/creator_central_spotify)**), in order to have access to the **Spotify API**.
- You can only provide **Spotify Tracks** *(Playlists / Albums / Podcasts are not supported)*

## Example

```javascript
const SpotifyToYoutubeMusic = require('spotify-to-ytmusic')

async function example() {

    // Set Spotify Credentials

    const spotifyToYoutubeMusic = await SpotifyToYoutubeMusic({
        clientID: "CLIENT_ID",
        clientSecret: "CLIENT_SECRET",
        accessToken: "ACCESS_TOKEN" // Optional
    })

    // Convert a Spotify Track

    let song = await spotifyToYoutubeMusic('4cOdK2wGLETKBW3PvgPWqT')
    console.log(song) // https://www.youtube.com/watch?v=lYBUbBu4W08
}

example()
```

*Other ways to provide a **Spotify Track**:*

```javascript
await spotifyToYoutubeMusic('https://open.spotify.com/track/4cOdK2wGLETKBW3PvgPWqT')

await spotifyToYoutubeMusic('spotify:track:4cOdK2wGLETKBW3PvgPWqT')

await spotifyToYoutubeMusic('https://api.spotify.com/v1/tracks/4cOdK2wGLETKBW3PvgPWqT')

await spotifyToYoutubeMusic(['4cOdK2wGLETKBW3PvgPWqT','06JvOZ39sK8D8SqiqfaxDU'])
```

## Note

This system is not 100% perfect, and sometimes will not get the right song(s) from YouTube Music.