# MP3 Life


# Sandisk Clip Sport Plus

## Playlists

* Use DOS ending for lines
* Use backward slashes (like windows)
* Folders start WIHOUT any prefix (./)

  Example:

```sh
#EXTM3U 
Music\Album\song1.mp3
Music\Album\song2.mp3
```

> Use `file playlist.m3u` to check that it is using the correct file format (ASCII text, with CRLF line terminators)

## Audiobooks

There are some issues with the file format when using `.m4b` and `.m4a`; the best way is to use `.mp3`, but simply renaming does not work well.

```sh
ffmpeg -i ebook.m4b -c:v copy -c:a libmp3lame -q:a 4 ebook.mp3
```



