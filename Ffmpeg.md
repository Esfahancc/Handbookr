# Install
```
yum install -y ffmpeg x265
```

## Convert to audio
```
ffmpeg -i <input> -vn -ar 44100 -ac 2 -ab 128k -f mp3 <output>
```

## Compress video
```
ffmpeg -i <input> -c:v libx265 -crf 28 -c:a aac -b:a 128k <output>
```

## Fast convert
```
ffmpeg -i <input> -vcodec copy -acodec copy <output>
```