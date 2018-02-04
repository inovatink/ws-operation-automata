# Operational State Diagram

This is work related to the operation of wearable sensor.

To modify code -> open [ws-state-diagram.tex](https://github.com/inovatink/ws-operation-automata/blob/master/ws-state-diagram.tex) with [sharelatex](https://www.sharelatex.com/).

![Alt text](https://github.com/inovatink/ws-operation-automata/blob/master/ws-state-diagram.png?raw=true "State Machine Diagram")

**Start** - Sensor is powered.

**Init** - This is what is going on in the Setup() of arduino program. Initialize peripherals, serial communication, sensors and modules.

**Config** - In this state the new configuration is done to the sample period, sensor selection and bluetooth related settings.

**Idle** - In this state device is idle data is sent to bluetooth and new sampling period didnt start yet.

**Sample** - Upon the start of new sample period sensor values are read.

**Serialize** - Sensor values are serialized to a string.

**Send** - Serialized string holding sensor values and timestamp is sent over Bluetooth.

**Receive** - In this state device checks for any new configuration sent over Bluetooth.




