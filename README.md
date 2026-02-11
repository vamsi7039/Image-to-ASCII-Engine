

**A free ascii image filter API** Just upload an image and get the image back in ascii characters!

![Untitled design(4)](https://user-images.githubusercontent.com/85095943/156201980-3eaee4ff-df7f-4653-926b-25f184ec1f41.png)



# How to use it ❓

Sample request using Python and the ```requests``` module:
```python
import requests
open("OUT_FILE.jpg", "wb").write(requests.post("https://imagscii.com/create/16/8", files={"file": open("FILE_TO_PROCESS.png", "rb")}).content)
```
The format for a request is the following:
```https://www.imagscii.com/create/FONT_SIZE/SPACING```

The same request using curl:
```curl -X POST -F file=@FILE_TO_PROCESS.png https://www.imagscii/create/16/8 >> OUT_FILE.png```
