# Object-Detection-App
A real-time object recognition application using [Google's TensorFlow Object Detection API](https://github.com/tensorflow/models/tree/master/research/object_detection) and [OpenCV](http://opencv.org/). The App detect the object appear in the Image or Video, It's optimize to detect from a video source/stream (RTMP/HLS).

<p align="center">
    <a href="https://github.com/Foxhound401/object-detection-app/blob/master/demo.png">
        <img alt="Demo Object Detection App" src="https://github.com/Foxhound401/object-detection-app/blob/master/demo.png"/>
    </a>
</p>

## Motivation
There have been several object detection applications, but some of them is rather slow or not optimize to work with video Streamming. So with the update of Tensorflow 1.14. We can make an attempt to optimize in order to raise the performance of the Tensorflow API.

## Requirements
- [Anaconda / Python 3.5](https://www.continuum.io/downloads)
- [TensorFlow 1.14](https://www.tensorflow.org/)
- [OpenCV 3.0](http://opencv.org/)


## Quick Start
Read futher to learn about how to install the environment for the app to run
install all the packages need to run the detection scripts
1. `conda env create -f environment.yml`
2. `python object_detection_app.py` 
    Optional arguments (default value):
    * Device index of the camera `--source=0`
    * Width of the frames in the video stream `-wd=480`
    * Height of the frames in the video stream `--height=360`
    * Number of workers `--num-workers=2`
    * Size of the queue `--queue-size=5`
    * Get video from HLS stream rather than webcam '--stream-input=http://somertmpserver.com/hls/live.m3u8'
    * Send stream to livestreaming server '--stream-output=--stream=http://somertmpserver.com/hls/live.m3u8'

## Streaming server using RTMP 

Stream file example-vid.mp4
` ffmpeg -re -i example-vid.mp4 -vcodec libx264 -vprofile baseline -g 30 -acodec aac -strict -2 -f flv rtmp://localhost/show/stream`

Link for the HLS stream 
http://localhost:8080/hls/stream.m3u8

* -re - consume stream on media's native bitrate (and not as fast as possible)
* -f - use video4linux2 plugin
* -i - select physical device to capture from
* -vcodec - specify video codec to output
* -vprofile - use x264 baseline profile
* -acodec - use aac audio codec
* -strict - allow using the experimental aac codec
* -f - specify format to output
* rtmp://localhost/show/stream - rtmp endpoint to stream to. if the target port is not 1935 is should be included in the uri.

bai tap ve nha 
ve mind map 
4 encapsulation inherit polymophysim abstraction

SOLID
