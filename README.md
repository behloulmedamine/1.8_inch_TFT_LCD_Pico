# 1.8_inch_TFT_LCD_Pico
ST7735_TFT_LCD library with an example demo 

# Hardware
- Raspberry Pi Pico
- ST7735_TFT_LCD(1.8_inch_TFT)

# Setup

Wiring details in "wiring.h"

# Requirements

install the following package.

```
sudo apt install cmake gcc-arm-none-eabi libnewlib-arm-none-eabi  libstdc++-arm-none-eabi-newlib build-essential
```

# Build the pico firmware

This project has a github actions workflow that build the Pico firmware. 

Othewise the project can be build with the following commmand, the `cmake` may take a couple of minutes.

```
mkdir build 
cd build
cmake ..
make -j8
```

# flash the RaspberryPi Pico

Drag and drop the src/simon.uf2 on the Pico in bootsel mode, or use the following command:

```
cp 1.8inch_TFT.uf2 /media/<user>/RPI-RP2/