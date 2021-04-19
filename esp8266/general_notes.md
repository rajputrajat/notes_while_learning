# Learning while working on esp8266-hal rust

## New terms

### CMSIS

* abbreviation of **Cortex Microcontroller Software Interface Standard**.
* it's vendor-independent hardware abstraction layer for mcs that are based on Arm Cortex processors.

### CMSIS-SVD

* CMSIS System View Description format
* describes the hardware features of microcontroller
* it lists all the peripherals available to the device
* where the registered associated to each device are located in memory and what's the function of each register
* these files are maintained by silicon vendors
* [reference](https://www.keil.com/pack/doc/CMSIS/SVD/html/index.html)
* format is based on xml. [example](https://www.keil.com/pack/doc/CMSIS/SVD/html/svd_Example_pg.html)

### svd2rust

* cli to transform SVD files into crates that expose type safe to access the peripherals of the device
* supports Cortex-M, MSP430 and RISCV microcontrollers

### MSRV

* minimum supported rust version
