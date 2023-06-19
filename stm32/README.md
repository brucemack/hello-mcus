Installation
============

Download and install STM32CubeMX
Download and install STM32CubeCLT
Download and install GNU Make for Windows

Download GNU Make for Windows
Download GNU Core Utils for Windows
Added the GNUWin32\bin folder to the PATH

Download OpenOCD and add to PATH

Download ARM cross-compilers and add to PATH 

Building
========

Added this to Makefile:
        
        openocd -f interface/stlink.cfg -f target/stm32f4x.cfg -c "program $(BUILD_DIR)/$(TARGET).elf verify reset exit"

Debug
=====
        openocd -f interface/stlink.cfg -f target/stm32f4x.cfg -c "program build/hello-stm32.elf verify reset"
        arm-none-eabi-gdb build/hello-stm32.elf
        target extended-remote localhost:3333
        


