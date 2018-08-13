# Arrows
An AI-ML Project that captures the images on the go via live video feed and classifies the image into labels using Inception-V3 pre-trained model along with Tensorflow. The video processing is done via OpenCV.

The aim of this project is to aid visually challenged people to know more about their surroundings. The image after classfication is converted to voice through TTS (Text-To-Speech) so they c

## Getting Started

Having a good internet connection is necessary and at least 200 MB of space for downloading the pre-trained Inception-V3 model.

### Prerequisites

1. Python 2.7+
2. OpenCV 3+
3. Tensorflow
4. [gTTS](https://github.com/pndurette/gTTS) (Google Text-To-Speech Engine)
5. Active Internet Connection

### Installing

After making sure that the above pre-requisites are met, clone this repository:
```
git clone https://github.com/AmitJoki/Arrows.git`
```
After cloning:
```
cd Arrows
python extract_images.py --pathIn=animals.mp4 --pathOut='images/'
```
The above will extract a frame for every one second of the given video and put them under images folder.
The images are stored in the format `frame{d}.jpg` format.

The output roughly looks like this:

![Screenshot](https://i.imgur.com/clplbv0.png)

As you can see, the good frames are frame6, frame18, frame23. The others will work too but will have a lesser accuracy.

Now, open a python shell or any IDE you prefer and make sure your Current Working Directory is Arrows and do:

```
>>> import classify_image;
>>> classify_image.run('images/frame6.jpg');
>>> classify_image.run('images/frame23.jpg');
>>> classify_image.run('images/frame18.jpg');
```

For every `classify_image.run()` check the Arrows folder for `out.mp3`. It contains the audio of the classified label.

You will be getting the output with high degree of accuracy and the classified label is outputted to the speaker via Google Text-To-Speech Engine.

## Milestones

1. Integrate all these snippets into one coherent program.
2. Use transfer-learning of Inception-V3 and train the model for more day-today activities.
3. Use further machine learning and identify good images and leave the noisy images.

## Resources
The image classification snippet is taken from Tensorflow's offical documentation to which I've made some few changes.
