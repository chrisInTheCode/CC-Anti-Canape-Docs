# Welcome to the Anti-Canape Docs!

Anti-Canape is an entire high-level interface for implementing CAN communication and, by extension, SDO Protocol. It contains several classes for reading and writing messages over CAN communication, provides support for several different drivers/dongles, and even includes an automator and script manager to assist with automation.


## Project layout

    main.py # The main program driver.
    drivers/
        readers.py # Provides reading functionality over CAN.
        writers.py # Provides writing functionality over CAN.
        dbcAutoParse.py # Provides parsing of DBC files.
        dotAutoParse.py # Provides parsing of DOT files.
        automator.py # Provides automation and script managing.



**Contact Information**  
Author: Chris Hinkson    
Email: Christopher.Hinkson@clubcar.com  
GitHub: https://github.com/chrisInTheCode/  