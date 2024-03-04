https://vanhunteradams.com/Pico/CourseMaterials/Building_Demos.html

[Getting started Pico](https://datasheets.raspberrypi.com/pico/getting-started-with-pico.pdf)

```bash
cd 
mkdir pico $ cd pico

// set up the sdk
$ git clone https://github.com/raspberrypi/pico-sdk.git --branch master 
$ cd pico-sdk 
$ git submodule update --init 
$ cd .. 
$ git clone https://github.com/raspberrypi/pico-examples.git --branch master


// Install toolchain
$ sudo apt update 
$ sudo apt install cmake gcc-arm-none-eabi libnewlib-arm-none-eabi build-essential

