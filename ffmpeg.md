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

## Merge 2 video file with same codec

- make a .txt file containing path to the files
```text
file video1.mp4
file video2.mp4
file video3.mp4
```
- convert each file to the same fps otherwise error will happen
	- here I am converting video1.mp4 to 3 fps
	- similarly do it for all the files
```bash
ffmpeg -i video1.mp4 -r 30 video1_30.mp4
```
- Now merge
```bash
ffmpeg -f concat -safe 0 -i files.txt -c copy output.mp4
```