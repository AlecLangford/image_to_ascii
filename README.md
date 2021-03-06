# image_to_ascii
A python script which converts gifs and images to ASCII

This python script converts images and gifs to ASCII

![demo](https://github.com/yattsu/image_to_ascii/blob/master/demo.gif)
![demo2](https://github.com/yattsu/image_to_ascii/blob/master/demo2.gif)
![demo3](https://github.com/yattsu/image_to_ascii/blob/master/demo3.png)

# Requirements
Python==3.8.1 <br>
Pillow==7.0.0 <br>
Requests==2.22.0

# Converting

To convert an image or GIF to ASCII, simply run: 
`python ascii.py /path/to/image.png` <br>
or <br>
`python ascii.py /path/to/image.jpg` <br>
or <br>
`python ascii.py /path/to/image.gif` <br>

It supports links aswell: <br>
`python ascii.py https://site.domain/image.png` <br>
or <br>
`python ascii.py https://site.domain/image.gif` <br>

If you don't add any more arguments, the image will be converted at full size. But you can add an integer after the image source to specify the percentage of the new image: <br>
`python ascii.py https://site.domain/image.png 50` - converts the image at half of its original size <br>
You can also add the `reverse` argument. This will invert the black and white of the image.
(If you use `reverse` you must specify the percentage of the image before like this `python ascii.py https://site.domain/image.png 50 reverse` or `python ascii.py https://site.domain/image.png 100 reverse` for the 1:1 scale)

Converting a GIF will result in creating a file for each frame inside of the `frames/` directory.

# Viewing an image / Playing a GIF

Once you converted the file, you can run `python show.py` to see your image/sequence of images.
If you don't add any more arguments, each frame of the GIF will be played at a 0.07s interval.
To change that, simply add the `s {interval}` argument like this `python show.py s 0.5`.
