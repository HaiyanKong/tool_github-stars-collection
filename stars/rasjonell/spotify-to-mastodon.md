---
project: spotify-to-mastodon
stars: 5
description: Show your currently playing Spotify track on Mastodon
url: https://github.com/rasjonell/spotify-to-mastodon
---

Spotify To Mastodon
===================

Show your currently playing Spotify track on Mastodon

Usage
=====

Clone the project and navigate to the project directory.

$ git clone https://github.com/rasjonell/spotify-to-mastodon
$ cd spotify-to-mastodon

Install dependencies

$ npm install

Change the `src/services/spotify.ts` file with your credentials.

const SpotifyClient \= new SpotifyAPI({
  clientId: '<YOUR CLIENT ID>',
  clientSecret: '<YOUR CLIENT SECRET>',
  accessToken: '<YOUR ACCESS TOKEN>',
  refreshToken: '<YOUR REFRESH TOKEN>',
});

Change the Mastodon instance URL in `src/index.ts`

const result \= await fetch(
  'https://<YOUR INSTANCE URL>/api/v1/accounts/update\_credentials',
  {...}

Run the service

npm run start

_Note: you might want to create a cron job to perform this script recurrently_
