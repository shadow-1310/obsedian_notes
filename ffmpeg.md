tags : #tool/media

### trimming video
```sh

ffmpeg -ss 00:01:00 -to 00:02:00 -i input.mp4 -c copy output.mp4

```
-  [documentation](https://trac.ffmpeg.org/wiki/Seeking#Cuttingsmallsections)
- [Cutting the videos based on start and end time using ffmpeg - Stack Overflow](https://stackoverflow.com/questions/18444194/cutting-the-videos-based-on-start-and-end-time-using-ffmpeg)

## convert audio codec from .mp3 to .aac
```bash
ffmpeg -i input.mp3 -c:a aac output.m4a
```

### swap audio content of a video file with another audio
```bash
ffmpeg -i input.mkv -i input.m4a -vcodec copy -acodec copy -map 0:0 -map 1:0 "final.mp4"
```