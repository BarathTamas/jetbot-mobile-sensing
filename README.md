# JetBot Mobile Sensing Experiment

## Introduction
A customized JetBot with a Jetson Nano 4GB board is used to perform measurements around a room. For the sensor used Adafruit's DHT-22 product, plugged into an Arduino Uno, which itself was plugged into the robot through a USB port.

## Road following demo
Video of road following with stop/move classification from the POV of the JetBot. Video is at ~3x real speed. At the sensor stops (green rectangles) the robot performs measurements for 10 second without processing images, hence the short "cuts".
In every frame, the JetBot has to 1. estimate where to go based on the marking tape (prediction marked with a red circle), 2. decide whether a stop has been reached. The robot is using a multi-tasking CNN (with EfficientNet b0 as the encoder), jointly retrained for the regression and classification tasks.

https://user-images.githubusercontent.com/44137494/129424808-45d1cc8e-4523-45ef-bdb2-94560483d9dd.mp4

## Output
The recorded measurements can be found in /data/measurements/merged_jetbot_data.csv. Due to low spatial and temporal variance in temperature/humidity in the monitored space, the data proved to be rather uninteresting.
