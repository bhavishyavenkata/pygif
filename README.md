# 🖼️ Team GIF Creator

This Python project creates an animated GIF from a set of PNG images using the `imageio.v3` library.

## 📌 What It Does

- Takes multiple team images (e.g., `team-pic1.png`, `team-pic2.png`)
- Combines them into a smooth animated `.gif`
- Sets the frame duration and looping options

## 🧠 Code Overview

```python
import imageio.v3 as iio

filenames = ['team-pic1.png', 'team-pic2.png']
images = []

for filename in filenames:
    images.append(iio.imread(filename))

iio.imwrite('team.gif', images, duration=500, loop=0)

duration=500 means 500ms per frame.

loop=0 makes the GIF loop infinitely.

Requirements
Install the required library using:
pip install imageio

 Files Required
Make sure the following images are in the same folder as your script:
team-pic1.png
team-pic2.png

How to Run
python create_gif.py

After running, you'll see a new file:
team.gif

