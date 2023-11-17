**Running A Script**

With the sdoAutomator and SdoScriptManager classes, running scripts is very easy and the majority of backend work is done for you. While custom scripts may have different arguments and operations, running them will generally follow the same instructions.

First, create a SdoScriptManager instance using the desired driver/dongle.

    myScriptManager = SdoScriptManager('pcan')

Next, simply call your script with whatever arguments it might have.

    myScriptManager = SdoScriptManager('pcan')

    myScriptManager.script_writeVehicleConfigActiveTest()

Most scripts implement a return value where True is a successful script operation and False is anything else (such as an error, exception, etc.). You could check if a script completes without error (but not necessarily that the output the script got is correct, unless incorrect output throws an error or stops execution in some manner) by checking the output:

    myScriptManager = SdoScriptManager('pcan')

    scriptSuccess = myScriptManager.script_writeVehicleConfigActiveTest()

    # Check if the script had an error or not
    if not scriptSuccess:
        print("Script encountered an error!")

While each script may be a little different in terms of arguments and return values, you can normally follow this style of running scripts.