### convert dir of images to pdf
```bash
convert *.jpg output.pdf
```
fix pdf conversion not working
- [stackoverflow](https://stackoverflow.com/questions/52998331/imagemagick-security-policy-pdf-blocking-conversion)

#### reduce quality
```bash
convert -quality 75 input.jpg output.jpg
```

#### convert to greyscale
```bash
convert input.jpg -colorspace output.jpg
```


convert input.pdf -format JPG -quality 10 output.pdf