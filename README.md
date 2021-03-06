# Paintkaro — A desktop Paint application in PyQt

## About the project
Express yourself with Paintkaro, the only painting programme where your art meets your imagination.

Paintkaro is a clone of the Paint programme from Windows with a few additions (and subtractions). The programme features standard tools including pen, brush, fill, spray can, eraser, text and a number of shapes.
## Screen shots
![Paintkaro](screenshot-paint1.jpg)
You can copy from the image, with a custom shape.The canvas is a fixed size and loaded images are adjusted to fit.
![Paintkaro](screenshot-paint2.jpg)
unique feature which we have in this application is you are free to hide and unhide tool box whenever you want.

## Built With
This application is made completely using python module pyqt5
* [Pyqt](https://pypi.org/project/PyQt5/)
## Getting Started
Download the folder run the main.py file
## Prerequisites
* pyqt
  ```sh
  pip install pyqt5
  ```
## Code notes
All tools are implemented with nested event handlers, which forward on events as appropriate. This allows for a lot of code re-used between tools which have common behaviours (e.g. shape drawing).
## Event handling
### Flood fill
This was the trickiest part of this app from a performance point of view. Checking pixels directly is far too slow (full-canvas fill time of approx 10 seconds). Most code to achieve this in Python sensibly uses numpy, but we didn't want to introduce a dependency for this alone.

By exporting the image as a bytestring, then down-sampling to a boolean byte-per-pixel (for match/no-match) to simplify the comparison loop, I could get it up to a reasonable speed.
The floodfillFunc is still pretty dumb though.
## Usage
* This application has many features where you can drag and drop shapes of your choice. 
* This application is used for painting,editing pictures.

## Contributors
