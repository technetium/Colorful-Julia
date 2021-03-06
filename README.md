# Colorful Julia Twitter Bot
<img src="saves/image_12222019_203050.png" alt="Julia set" width="250"/>
Colorful Julia is a Twitter bot that tweets random Julia sets. Along with the image itself, the tweet also includes information about the rendered Julia set, such as the maximum amount of iterations, value of c, and the colorization method. Colorful Julia uses the tweepy wrapper to communicate with the Twitter API.

Go check out the bot: https://twitter.com/colorjulia_bot

## Installation
Clone repo:
``` 
~$ git clone https://github.com/Visual-mov/ColorfulJulia
```

Install requirements:
```
~$ pip3 install -r requirements.txt
```

## Running
Run main script:
```
~$ python3 colorful_julia.py [--date_img] [--no_tweet] [--path p]
```
**'--path p'** - Give different path to save images. Default path is *./saves*

**'--date_img'** - Save each Julia set image with a unique date and time code instead of overwriting previous image.

**'--no_tweet** - Will not tweet created image. Access keys will also not be given to the Twitter API.

## Hosting
Currently, the bot is being hosted on a Raspberry Pi Zero. The main script is run every 30 minutes using a cron job.
```
*/30 * * * * python3 ./Colorful-Julia/colorful_julia.py
```
