# Multi-Shifter
This fork of Keyboard-H-Shifter was created for sim racing games to simulate an Automatic and/or H-Shifter DirectInput device using a keyboard (physical or [simulated](https://github.com/ThreeDeeJay/FFShifter))

To use this app you need to:
- Install [vJoy](https://sourceforge.net/projects/vjoystick/)
- Configure the first vJoy device with 32 total buttons.
- Install [Python 3.8](https://www.python.org/ftp/python/3.8.0/python-3.8.0-amd64.exe)
- Run 'Multi-Shifter.cmd'
- If needed, change which keys will trigger which vJoy device buttons then **End** and **Start** to apply changes, then **Save settings**.
- In the game input options, map the vJoy device button to the desired gears.

# How does it work?
Using tidzo's library pyvjoy(https://github.com/tidzo/pyvjoy) we can modify the state of vJoy buttons, and with the help of 'pynput' we can bind those commands to keyboard buttons. The way that it works is that once you click the 'gear' button on your keyboard, it will simulate a continuos press of a vJoy device button. Example: by pressing '1' with default settings in the app you will simulate '1' button in the vJoy and it will not release itself until you press another gear or neutral, which releases all the buttons.
NOTE: if you want to run and build it yourself, you have to extract the 'dont_steal_this.ico' from the rar file and place it in the same folder with main.py in order for it to work
