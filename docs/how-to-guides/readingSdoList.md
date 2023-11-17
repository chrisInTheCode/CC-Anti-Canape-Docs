**Read a List of SDO Parameters**

Reading a list of SDO parameters is very efficient with the SdoAutomator class. First, get a bus object for your driver with the ScriptManager.getDefaultBus() method.

    # Get bus for specified driver
    myBus = ScriptManager.getDefaultBus('pcan')

Then, create reader and writer objects and then use them to make the automator object.

    # Get bus for specified driver
    myBus = ScriptManager.getDefaultBus('pcan')

    # Get reader and writer
    myReader = ACReader(mybus)
    myWriter = ACWriter(mybus)

    # Create automator
    myAutomator = sdoAutomator(reader, writer)

Next, call readSdoList() to read the current values of each SDO parameter in the list. It will return a Pandas dataframe of parameters and values.

    # Create automator
    myAutomator = sdoAutomator(reader, writer)

    # Read SDO Parameter Values
    returnDataFrame = myAutomator.readSdoList([parameter1, parameter2, ...])

By default, this method will print out the parameter values to the terminal. You can disable this by passing the optional argument doPrint=False.

    # Read SDO Parameter Values
    returnDataFrame = myAutomator.readSdoList([parameter1, parameter2, ...], doPrint=False)