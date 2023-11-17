# CC-Anti-Canape-Docs

This application provides reading and writing functionality for CAN Messages, and in extension, SDO Protocol over CAN Messages. It supports kvaser, pcan, and vector drivers for all functionality. It also incorporates a custom DBC parser,a custom DOT parser, and an automator/script manager for automation purposes.

Installation Instructions:

    Move the entire project to the desired directory location
    Install all of the required python packages using `pip install requirements.txt``

NOTE: This project is still under heavy development. There may be unknown bugs in the program. Myself, Christopher Hinkson, and the company, Club Car LLC, are not liable for any bugs and/or unexpected operations that occur within this program.

How To Use:

    You may use this project as a terminal-based application
    You may use this as a script creator and executor for simple actions and automations
    You may use this as a behind-the-scenes framework to develop a user-focused application with
    You may use this as a framework for integrating into other python programs and embed extra functionality alongside during deployment.

This framework provides basic reading and writing abilities for CAN communication in python:

    It includes several methods for reading and writing CAN messages one-time, periodically, and continously
    It also includes configurations to communicate with kvaser dongles, pcan dongles, and vector dongles
    It has tie-ins for storing data, logging data, and graphically displaying data (these are not included in the base package, but the architecture has been designed to accompany these additions)
    It is still in a maintenceable development architure, with extended documentation along with direct links for all resources

It is highly suggested that you review the docs included in this project for any referencing you need. If you are unable to find what you are looking for, I suggest checking the github repo or contacting me at the below contact information.

_Contact Information_
Author: Christopher Hinkson 
Email: Christopher.Hinkson@clubcar.com 
GitHub: https://github.com/chrisInTheCode
