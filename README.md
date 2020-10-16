# spotify-playlist-archive [![Build Status](https://travis-ci.com/mackorone/spotify-playlist-archive.svg?branch=master)](https://travis-ci.com/mackorone/spotify-playlist-archive)

> Daily snapshots of public Spotify playlists

Spotify's playlists are great. I like that they're updated once in a while -
change is good! I don't like, however, that it's impossible to see older
versions. How am I supposed to remember the name of that song I really liked?
Apparently, I'm not alone: see
[here](https://community.spotify.com/t5/Content-Questions/View-previous-versions-of-playlists/td-p/4400750),
[here](https://community.spotify.com/t5/Accounts/A-playlist-was-modified-Can-I-get-the-old-songs-back/td-p/1001889),
[here](https://community.spotify.com/t5/Content-Questions/Seeing-an-old-version-of-a-playlist/td-p/1318739),
[here](https://community.spotify.com/t5/Other-Partners-Web-Player-etc/Playlists-Is-there-any-way-to-recover-previous-versions-of-a/td-p/4726831),
[here](https://community.spotify.com/t5/Desktop-Mac/Find-Songs-of-old-versions-of-Spotify-Playlists/td-p/998504),
[here](https://community.spotify.com/t5/Closed-Ideas/Playlist-Versioning-History/idi-p/1133819),
[here](https://community.spotify.com/t5/Closed-Ideas/Playlist-History-Versioning/idi-p/1346418),
[here](https://community.spotify.com/t5/Closed-Ideas/Playlists-Playlist-History/idi-p/1816799),
and [here](https://community.spotify.com/t5/Live-Ideas/Playlists-Edit-History/idi-p/4573743).
Since Spotify won't take snapshots of our favorite playlists, let's do it ourselves!

## Quick start

1. To view the current version of a playlist, click on its name below
1. To see all songs that ever belonged to a playlist, click "cumulative"
1. To determine which songs were added or removed from a playlist, click "githistory"
1. To add a playlist to the archive, simply `touch playlists/plain/<playlist_id>` and make a pull request

## How it works

This reposity contains a script for scraping Spotify playlists and publishing
them back to the repo. The script is run daily via
[Travis CI](https://travis-ci.com/mackorone/spotify-playlist-archive)
(free for public GitHub repos). It's also run after every commit, which means
that playlists get regenerated whenever the scraping or formatting logic
changes, or when new playlists are added - cool!

The script determines which playlists to scrape by looking at the file names in
`playlists/plain`. Anything that's not a valid playlist ID gets removed. Files
that *are* a valid playlist IDs get regenerated: a pretty version of each
playlist gets dumped in `playlists/pretty`, new tracks are added to the
files in `playlists/cumulative`, and a plaintext version of each playlist is
written back to `playlists/plain`. The plain version is sorted alphabetically,
rather than by track number, so that it only changes when tracks are added or
removed, making [Git History](https://githistory.xyz/) a nice way to visualize
how the playlist evolves over time.

The list below is autogenerated.

## Playlists

- [Chill Pop
](https://github.com/catzs/spotify-playlist-archive/blob/master/playlists/pretty/Chill%20Pop
.md)
- [Just Good Music
](https://github.com/catzs/spotify-playlist-archive/blob/master/playlists/pretty/Just%20Good%20Music
.md)
