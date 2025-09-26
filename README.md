# Air-quality-UI
1. WHO data show that almost all of the global population (99%) breathe air that exceeds WHO guideline limits and contains high levels of pollutants, with low- and middle-income countries suffering from the highest exposures.
2. More than 80% of people living in urban areas that monitor air pollution are exposed to air quality levels that exceed WHO limits.

## System description and operation
### Hardware
1. ESP32 microcontroller
2. Grove - Gas Sensor V2 (Multichannel)
### Libraries
You will need to install the following libraries to run the Python code:
1. tkinter: main module to create GUI
2. pySerial: to get sensor data from the microcontroller
3. functools: to flatten functions with multiple parameters
4. NumPy: Fundamental package for scientific computing with Python.
5. pandas: A powerful data analysis and manipulation library.

## How to use it?
### With Hardware
1. Upload the Arduino code “gas_sensor.ino” with the ESP32-WROOM-DA Module as the selected board.
<img width="1193" height="880" alt="image" src="https://github.com/user-attachments/assets/2aaeaa32-fb27-4085-86f8-ae35aa6f24c6" />

2. Once uploaded successfully, close the Arduino IDE. The same device & port can not be accessed by the different IDEs at the same time.
3. Run the Python program “mainGUI.py”. Make sure you have entered the correct port name and baud rate.
<img width="1194" height="650" alt="image" src="https://github.com/user-attachments/assets/1820fbc5-5d4f-42e1-a316-b3975c7cb7d7" />


### Without Hardware (on stored data)
If you do not have the hardware, you may run the test code.
1. Comment out the dispData() call, and uncomment the testDispData() in “mainGUI.py”.<br />
**From**<br />
<img width="910" height="373" alt="image" src="https://github.com/user-attachments/assets/f47da486-397d-466f-9922-ed06ea08d7c4" />
<br />
  **to**<br />
<img width="929" height="369" alt="image" src="https://github.com/user-attachments/assets/ee73a8d6-5f5b-4d3e-a747-9d73d3612f39" />

2. Change the value of the parameter manually from 0 to 11 to check the program for changing gas values. Run the program **mainGUI.py**; no need to run **gas_sensor.ino**.

<img width="1127" height="971" alt="image" src="https://github.com/user-attachments/assets/4755a8a0-294c-401c-bbb1-41c2f131c2c4" />
<img width="1126" height="967" alt="image" src="https://github.com/user-attachments/assets/f7a33e11-da7a-41a3-a318-df4e1564121c" />

*The colours are assigned based on the standards laid out by the [U.S. Environmental Protection Agency](https://www.airnow.gov/sites/default/files/2020-05/aqi-technical-assistance-document-sept2018.pdf)*

3. The  “?” button is displayed whenever the concentrations of the gas reach levels that are not healthy. Clicking on the button displays the possible sources, effects on health & precautionary measures.

<img width="676" height="985" alt="image" src="https://github.com/user-attachments/assets/a881e8f4-c854-45da-ad72-f88fc6f0bfd0" />
<img width="674" height="555" alt="image" src="https://github.com/user-attachments/assets/f1e51b53-12bc-4fe5-964e-fd0fd0ac8679" />

