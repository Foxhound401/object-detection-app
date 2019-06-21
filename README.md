# Object-Detection-App

A real-time object recognition application using [Google's TensorFlow Object Detection API](https://github.com/tensorflow/models/tree/master/research/object_detection) and [OpenCV](http://opencv.org/).

## Requirements
- [Anaconda / Python 3.5](https://www.continuum.io/downloads)
- [TensorFlow 1.2](https://www.tensorflow.org/)
- [OpenCV 3.0](http://opencv.org/)


## Quick Start
install all the packages need to run the detection scripts
1. `conda env create -f environment.yml`
2. `python object_detection_app.py` / `python object_detection_multithreading.py`
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

* -re - consume stream on media's native bitrate (and not as fast as possible)
* -f - use video4linux2 plugin
* -i - select physical device to capture from
* -vcodec - specify video codec to output
* -vprofile - use x264 baseline profile
* -acodec - use aac audio codec
* -strict - allow using the experimental aac codec
* -f - specify format to output
* rtmp://localhost/show/stream - rtmp endpoint to stream to. if the target port is not 1935 is should be included in the uri.

Link for the HLS stream 
http://localhost:8080/hls/stream.m3u8

bai tap ve nha 
ve mind map 
4 encapsulation inherit polymophysim abstraction

SOLID
