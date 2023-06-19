Hardware Setup
==============

You need the CP210x USB to UART Bridge Virtual COM Port (VCP) driver to see the ESP32 module 
as a COM port.  This is located on the Silicon Labs website.

Setup For esptool
=================

One time setup:

        python3 -m venv dev
        dev\scripts\activate
        pip install esptool


Espressif Toolchain Installation
================================

Downloaded ESP-IDF v5.0.2 Offline Installer and run.

Don't let the installer add any more drivers (this was done already).

This installer will create a CMD and PowerShell shortcut that has all necessary environment variables.

Building A Project
==================

        idf.py set-target esp32
        idf.py build
        idf.py -p COM9 flash
        idf.py -p COM9 monitor


