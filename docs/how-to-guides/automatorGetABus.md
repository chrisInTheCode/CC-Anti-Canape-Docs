**Get a default bus in the Script Manager class**

Getting a default bus is very fast and easy with the getDefaultBus() method included with the Script Manager class. Simply create a new ScriptManager instance and call the method.

    # Create a new instance with your driver/dongle
    myNewScriptManagerInstance = SdoScriptManager('pcan') 
    
    # Get a bus for the instance
    myNewBus = myNewScriptManagerInstance.getDefaultBus(myNewScriptManagerInstance.bus)

You can also call the method directly to get a bus.

    # Get a bus for your driver/dongle
    myNewBus = SdoScriptManager.getDefaultBus('pcan') 

Getting a bus is even easier when done so in a script. See the [Adding to the Script Manager](./addAScript.md) how-to guide for information on getting a bus within a custom script.