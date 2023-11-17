**Project Tutorial**

This project can be implemented in a variety of ways. It can be used just as a base framework to support a larger, more user-focused application. It can also be used for automation scripting without any other dependencies. It can even be used just as-is for communicating over CAN protocols.

Because of the wide range of possible uses, providing a tutorial is not the clearest insight into how to use the program. Because of this, I will provide a single tutorial that runs all three currently-existing scripts. For further guides on how to use each part of Anti-Canape, I suggest checking out the source code (which is heavily documented in the References tab) along with the How-To-Guides page.  

  

**Scripting Tutorial**  
*The ScriptManager class makes it very easy to run scripts. Here is the total code for running all three scripts *:  

    '''
    CC Anti-Canape: Python-CAN Interface Application

    Author: Chris Hinkson
    Email: Christopher.Hinkson@clubcar.com

    Desc: This application is designed to provide reading access to CAN communication from within python as a standalone application.

    Github: https://github.com/chrisInTheCode/CC-Anti-Canape
    --> To get access to the github repository, please send me an email at the above address

    References:
    --> https://python-can.readthedocs.io/en/stable/
    --> https://cantools.readthedocs.io/en/latest/
    '''
    if __name__ == '__main__':
        ''' This script provides a convenient location to test the framework, build additional architecture, and use the various scripts from the script manager. The below steps will only run if this is the main program (this program was directly run by the program).
        '''
        ##################
        # MODULE IMPORTS #
        ##################
        import sys

        ##################
        # DRIVER IMPORTS #
        ##################
        sys.path.append('drivers')
        from drivers.automator import SdoScriptManager

        ##########################
        # MAIN PROGRAM EXECUTION #
        ##########################
        try:
            # Get a Script Manager Object
            scriptManager = SdoScriptManager(driver="pcan")

            # Run the three current scripts
            scriptManager.script_writeVehicleConfigActiveTest()
            scriptManager.script_writeDstTest()
            scriptManager.script_configureSdo()

        # For terminating the program
        except KeyboardInterrupt:
            print("CC Anti-Canape: Program Execution Halted by Keyboard Interrupt!")