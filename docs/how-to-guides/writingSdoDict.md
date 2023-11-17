**Write a Dictionary of SDO Parameters and Values**

Writing a dictionary of SDO parameters and values is very efficient with the SdoAutomator class. First, get a bus object for your driver with the ScriptManager.getDefaultBus() method.

    # Get bus for specified driver
    myBus = ScriptManager.getDefaultBus('pcan)

Then, create reader and writer objects and then use them to make the automator object.

    # Get bus for specified driver
    myBus = ScriptManager.getDefaultBus('pcan')

    # Get reader and writer
    myReader = ACReader(mybus)
    myWriter = ACWriter(mybus)

    # Create automator
    myAutomator = sdoAutomator(reader, writer)

Next, call writeSdoDict() to write the dictionary of parameters and values. It will return a Pandas dataframe of initial read values, written values, and final read values.

    # Create automator
    myAutomator = sdoAutomator(reader, writer)

    # Write SDO Dictionary
    returnDataFrame = myAutomator.writeSdoDict({param1:value1, param2:value2, ...})

You can also (optionally) include a timeDelay argument, which will change the time in between each SDO message. This defaults to 0.03s, which is recommended for normal use. If you wish to change it, you can call writeSdoDict() as such:

    # Write SDO Dictionary
    returnDataFrame = myAutomator.writeSdoDict({param1:value1, param2:value2, ...}, timeDelay=???)

By default, this method will print out the results to the terminal. You can disable this by passing the optional argument doPrint=False.

    # Write SDO Dictionary
    returnDataFrame = myAutomator.readSdoList({param1:value1, param2:value2, ...}, doPrint=False)