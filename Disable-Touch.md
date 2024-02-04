# Disable Touch
The Marauder v6 and v6.1 both feature two physical buttons on the back of their enclosures. One button functions as a hard reset button and the other controls the state of the GPIO0 pin of the ESP32. By default, these two buttons are intended to be used to control the boot mode of the ESP32. During typical Marauder firmware runtime, the button controlling GPIO0 can be used to disable the touch input of the screen. This feature is especially useful during scans when you want to place the Marauder in your pocket or backpack and don't want the scan to close accidentally. The touch input can be enabled or disabled at anytime regardless of the Marauder's current operation.

#### To Enable/Disable touch input
Hold the GPIO0 button for >=1sec