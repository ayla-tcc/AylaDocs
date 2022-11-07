# AylaDocs
This is documentation intended to give instructions and further explain how Ayla works. Besides the documentation, it will also be available separately in the respective repos. \
\
***This document will be updated on in my spare time* 

## 📚 Table of Contents
   - [Hospital-screening](#🧶-hospital-screening)
      - [Arduino for screening](#🤖-arduino-for-screening)
      - [PyAPI](#🐍-pyapi)
   - [Web](#🏀-web)

## 🧶 Hospital-screening
Available at [Hospital-Screening repo](https://github.com/ayla-tcc/Hospital-screening)
### 🌼 How  the screening process works

Will be added soon

### 🤖 Arduino for screening
Inside the folder `Arduino` you can access clicking [here](https://github.com/ayla-tcc/Hospital-screening/tree/main/Arduino) \

After that, you need to install the Arduino IDE, you can download it [here](https://www.arduino.cc/en/software). \
\
At first you need at least 2unit *Arduino UNO*, 1unit *MX30102* (Heart Rate Sensor for Arduino) and  *MLX90614* (Temperature Sensor for Arduino) but you can check if the cable connections are working properly by clicking [here](https://wokwi.com/) (This is a simulator for Arduino and will be updated). \
\
The `lib` folder contains the necessary libraries for the sensors and can be installed by copying their contents and pasting them at `C:\Users'/Documents'/Arduino/libraries`.  \
\
The `src` folder contains the code for the Arduino in the folders with their respective sketch names, you can open it with the Arduino IDE and load it into the Arduino. \
\
I advise you to write down the respective COM ports since you will be asked for them in the  [PyAPI](#🐍-pyapi) topic.

---
How see the data from the sensors?\
How know if the COM port in Windows?\
Will be add soon

---

### 🐍 PyAPI
Inside the folder `pyapi` you can access clicking [here](https://github.com/ayla-tcc/Hospital-screening/tree/main/pyApi)
#### Requirements

- Python 3.8 or higher
- pip
- git
```bash
pip install -r requirements.txt
# Available at this repository
```
#### Editing the files for your usage
You need to edit the `serialMX.py` *(Heart Rate Sensor)*, `serialTemp` *(Temperature Sensor)* file, you can find it at `Hospital-screening/pyApi/` \
\
You need to change the `porta` variable to the respective COM port of the Arduino that you wrote down in the [Arduino for screening](#🤖-arduino-for-screening) topic. \
Like this:
```python
porta = "COM3"
# Change the COM3 to the respective COM port
```
#### Running
```bash
# Frist Clone the repository
git clone https://github.com/ayla-tcc/Hospital-screening.git
# Then go to the folder
cd ./pyApi
# Run the server
python -m uvicorn main:app --reload --host 0.0.0.0 --port 8000
```
#### Testing
1. Go to [Localhost](http://127.0.0.1:8000/docs)

## 🏀 Web
Available at [ayla-tcc.github.io](https://github.com/ayla-tcc/ayla-tcc.github.io) \
We use github-pages to host this page


