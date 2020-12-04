# ObjectDetection using TensorFlow Lite

## Introduction
This is source code for running Tensor Flow Lite to run sample object detection model on Raspberry Pi or any other Linux based operating system

## Prerequisites
- Create virtual python environment so that other programs are not affected
```
sudo pip3 install virtualenv
python3 -m venv tflite-env
source tflite-env/bin/activate
```

- Install required libraries
```
pip install opencv-python
pip install https://github.com/google-coral/pycoral/releases/download/release-frogfish/tflite_runtime-2.5.0-cp37-cp37m-linux_x86_64.whl  //For Raspberry Pi
pip install https://github.com/google-coral/pycoral/releases/download/release-frogfish/tflite_runtime-2.5.0-cp37-cp37m-macosx_10_15_x86_64.whl // For Mac OS
```

- Downloading Google’s TFLite Model:
```
wget https://storage.googleapis.com/download.tensorflow.org/models/tflite/coco_ssd_mobilenet_v1_1.0_quant_2018_06_29.zip

unzip coco_ssd_mobilenet_v1_1.0_quant_2018_06_29.zip -d object_detect_model
```

## Run The program:
```
python3 TFLite_detection_webcam.py --modeldir ../Sample_TFLite_model
```



## References
Code is based on the repo : https://github.com/EdjeElectronics/TensorFlow-Lite-Object-Detection-on-Android-and-Raspberry-Pi/blob/master/Raspberry_Pi_Guide.md
