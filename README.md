# Automatic-Number-Plate-Recognition-YOLOv8
## Demo


https://github.com/Muhammad-Zeerak-Khan/Automatic-License-Plate-Recognition-using-YOLOv8/assets/79400407/1af57131-3ada-470a-b798-95fff00254e6



## Data

The video I used in this tutorial can be downloaded [here](https://drive.google.com/file/d/1JbwLyqpFCXmftaJY1oap8Sa6KfjoWJta/view?usp=sharing).

## Model

A Yolov8 pre-trained model (YOLOv8n) was used to detect vehicles.

A licensed plate detector was used to detect license plates. The model was trained with Yolov8 using [this dataset](https://universe.roboflow.com/roboflow-universe-projects/license-plate-recognition-rxg4e/dataset/4). 
- The model is available [here](https://drive.google.com/file/d/1Zmf5ynaTFhmln2z7Qvv-tgjkWQYQ9Zdw/view?usp=sharing).

## Dependencies

The sort module needs to be downloaded from [this repository](https://github.com/abewley/sort).
## WSL2 setup
```bash
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt-get update
sudo apt-get install python3.8
sudo apt install python3.8-venv
```
## Wsl2 other dependencies
```bash
sudo apt-get install python3.8-dev
sudo apt-get install gcc
sudo apt-get install libssl-dev libffi-dev      libxml2-dev libxslt1-dev zlib1g-dev
sudo apt install g++
sudo apt-get install python3.8-tk
```
* install sort module from [this repository](https://github.com/abewley/sort)





## Project Setup

* Setup virtual environment 
```bash
python3.8 -m venv lprenv
```
* Activate environment
source lprenv/bin/activate

* Install the project dependencies using the following command 
```bash
pip install -r requirements.txt
```
* Download sample video file from [here](https://drive.google.com/file/d/1JbwLyqpFCXmftaJY1oap8Sa6KfjoWJta/view?usp=sharing)

* Run main.py with the sample video file to generate the test.csv file
``` python
python main.py
```

## Visualizing result

* Run the add_missing_data.py file for interpolation of values to match up for the missing frames and smooth output.
```python
python add_missing_data.py
```

* Finally run the visualize.py passing in the interpolated csv files and hence obtaining a smooth output for license plate detection.
```python
python visualize.py
```
