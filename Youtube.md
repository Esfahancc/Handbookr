# Install
```
yum install -y youtube-dl
```

## Playlist
```
youtube-dl --ignore-errors --proxy socks5://127.0.0.1:9050 -o '%(playlist)s/%(title)s.%(ext)s' <playlist_link>
```

## Audio
```
youtube-dl --ignore-errors --proxy socks5://127.0.0.1:9050 -o '%(title)s.%(ext)s' --extract-audio --audio-format mp3 --audio-quality 128K <video_link>
```