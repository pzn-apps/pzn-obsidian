---
{"dg-publish":true,"permalink":"/pzn-apps/en/talent-content-mgmt/spotify-api-bridge/"}
---

## Spotify API Bridge
Parses meta-data from Spotify API as well as provides access to some features unavailable in Spotify's Public API, such as [[pzn-apps/en/talent-content-mgmt/Spotify API Bridge#User's Playlist Creation Modification\|User's Playlist Creation/Modification]] and [[pzn-apps/en/talent-content-mgmt/Spotify API Bridge#Playcount Statistics\|Playcount Statistics]]. 
Also includes a bottle-neck rate-limit control, useful for 
massive [[pzn-apps/en/talent-content-mgmt/Spotify API Bridge#Spotify Content Meta-data Parsing\|Spotify Content Meta-data Parsing]].
Intelligently saves parsed to data to relevant table and records in [[pzn-apps/en/talent-content-mgmt/Talent and Content Management System#Catalog base\|Catalog base]]

#### User's Playlist Creation/Modification
Connects to a Spotify Account to create/modify/unsubscribe user's playlist via [[pzn-apps/en/talent-content-mgmt/Monito.website Data Hub\|Monito.website Data Hub]]. Useful for managing and easy updating of a multi-playlist network.
![pzn-apps/img/Pasted image 20220509200037.png](/img/user/pzn-apps/img/Pasted%20image%2020220509200037.png)
![pzn-apps/img/Pasted image 20220509195914.png](/img/user/pzn-apps/img/Pasted%20image%2020220509195914.png)

#### Playcount Statistics
![pzn-apps/img/Screenshot 2022-05-09 at 19.53.51.png](/img/user/pzn-apps/img/Screenshot%202022-05-09%20at%2019.53.51.png)
![pzn-apps/img/Pasted image 20220509195241.png](/img/user/pzn-apps/img/Pasted%20image%2020220509195241.png)

#### Spotify Content Meta-data Parsing
![pzn-apps/img/Pasted image 20220508195842.png](/img/user/pzn-apps/img/Pasted%20image%2020220508195842.png)
Available actions:
- Get Album's Tracks
- Get Playlist's Tracks
- Get Album' 
- Get Tracks features
	- Codes, ISRC etc
	- Musical and Mood data
- Get User's Playlists
![pzn-apps/img/Screenshot 2022-05-09 at 18.35.47.png](/img/user/pzn-apps/img/Screenshot%202022-05-09%20at%2018.35.47.png)


<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">




# Spotify API Bridge
## Indices
* [get album data](#1-get-album-data)
* [get album tracks](#2-get-album-tracks)
* [get albums data](#3-get-albums-data)
* [get albums tracks](#4-get-albums-tracks)
* [get track audio analysis](#5-get-track-audio-analysis)
* [get track audio features](#6-get-track-audio-features)
* [get track data](#7-get-track-data)
* [get tracks audio analysis](#8-get-tracks-audio-analysis)
* [get tracks audio features](#9-get-tracks-audio-features)
* [get tracks data](#10-get-tracks-data)
* [get user playlists](#11-get-user-playlists)


--------


### 1. get album data



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: https://monito.website/controller/v2/webhook/spotify/getAlbum
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| x-api-key | 12345678 |  |



***Body:***

```js        
{
    "uri": "spotify:album:3DaF23bfsiWlqR6T5lqq9b"
}
```



### 2. get album tracks



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: https://monito.website/controller/v2/webhook/spotify/getAlbumTracks
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| x-api-key | 12345678 |  |



***Body:***

```js        
{
    "uri": "spotify:album:3DaF23bfsiWlqR6T5lqq9b"
}
```



### 3. get albums data



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: https://monito.website/controller/v2/webhook/spotify/getAlbums
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| x-api-key | 12345678 |  |



***Body:***

```js        
{
    "albumsUris": ["spotify:album:3DaF23bfsiWlqR6T5lqq9b","spotify:album:0tgCzdxlaRL3X0wxBpSKy4"]
}
```



### 4. get albums tracks



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: https://monito.website/controller/v2/webhook/spotify/getAlbumsTracks
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| x-api-key | 12345678 |  |



***Body:***

```js        
{
    "albumsUris": ["spotify:album:3DaF23bfsiWlqR6T5lqq9b","spotify:album:0tgCzdxlaRL3X0wxBpSKy4"]
}
```



### 5. get track audio analysis



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: https://monito.website/controller/v2/webhook/spotify/getAudioAnalysisForTrack
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| x-api-key | 12345678 |  |



***Body:***

```js        
{
    "uri": "spotify:track:3fVtTWBglCCrWh5siXWTrd"
}
```



### 6. get track audio features



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: https://monito.website/controller/v2/webhook/spotify/getAudioFeaturesForTrack
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| x-api-key | 12345678 |  |



***Body:***

```js        
{
    "uri": "spotify:track:3fVtTWBglCCrWh5siXWTrd"
}
```



### 7. get track data



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: https://monito.website/controller/v2/webhook/spotify/getTrack
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| x-api-key | 12345678 |  |



***Body:***

```js        
{
    "uri": "spotify:track:3fVtTWBglCCrWh5siXWTrd"
}
```



### 8. get tracks audio analysis



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: https://monito.website/controller/v2/webhook/spotify/getAudioAnalysisForTracks
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| x-api-key | 12345678 |  |



***Body:***

```js        
{
    "tracksUris": ["spotify:track:3fVtTWBglCCrWh5siXWTrd", "spotify:track:0ozX6sHcnVJrZh8c9PUCF2"]
}
```



### 9. get tracks audio features



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: https://monito.website/controller/v2/webhook/spotify/getAudioFeaturesForTracks
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| x-api-key | 12345678 |  |



***Body:***

```js        
{
    "tracksUris": ["spotify:track:3fVtTWBglCCrWh5siXWTrd", "spotify:track:0ozX6sHcnVJrZh8c9PUCF2"]
}
```



### 10. get tracks data



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: https://monito.website/controller/v2/webhook/spotify/getTracks
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| x-api-key | 12345678 |  |



***Body:***

```js        
{
    "tracksUris": ["spotify:track:3fVtTWBglCCrWh5siXWTrd", "spotify:track:0ozX6sHcnVJrZh8c9PUCF2"]
}
```



---



### 11. get user playlists



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: https://monito.website/controller/v2/webhook/spotify/getUserPlaylists
```


***Headers:***

| Key | Value | Description |
| --- | ------|-------------|
| x-api-key | 12345678 |  |



***Body:***

```js        
{
    "userUri": "spotify:user:11oxogowtluq6ispny1q1f34u"
}
```



---
[Back to top](#spotify)


</div></div>


----
[[pzn-apps/en/talent-content-mgmt/Catalog Base\|Back to Catalog base]]