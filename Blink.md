[source](https://datasheets.raspberrypi.com/pico/getting-started-with-pico.pdf)

From the pico directory we created earlier, navigate into pico-examples and create a build directory: 


```bash
cd pico-examples 
mkdir build $ cd build
```

Then set the PICO_SDK_PATH, assuming you cloned the pico-sdk and pico-examples repositories into the same directory: 

```bash
export PICO_SDK_PATH=../../pico-sdk
```



For the Pico Prepare your cmake build directory by running the following command: ```
```bash
cmake .. Using PICO_SDK_PATH from environment ('../../pico-sdk') 
```
`PICO_SDK_PATH is /home/pi/pico/pico-sdk   .   .   . -- Build files have been written to: /home/pi/pico/pico-examples/build 

You can now type make to build all example applications. However, for this example we only need to build blink. To build a specific subtree of applications, navigate into the corresponding subtree before running make. In this case, we can build only the blink task by first navigating into the blink directory, then running make: 

`$ cd blink` 
`$ make -j4` 

`Scanning dependencies of target ELF2UF2Build Scanning dependencies of target boot_stage2_original [ 0%] Creating directories for 'ELF2UF2Build'   .   .   . [100%] Linking CXX executable blink.elf [100%] Built target blink  TIP Invoking make with -j4 speeds the build up by running four jobs in parallel. A Raspberry Pi 5 has four cores, so four jobs spreads the build evenly across the entire SoC. Amongst other targets, this builds: blink.elf used by the debugger blink.uf2 the file we’ll copy onto RP2040 USB Mass Storage Device`
