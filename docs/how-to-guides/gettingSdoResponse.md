**Get SDO Response Message**

Getting a SDO Response Message is very easy with the ACReader getSdoResponse() method. Everything has already been automated for you, all you have to do is call the method.

    # Create a new ACReader object with a (pre-defined) bus
    myReader = ACReader(bus)

    # Get the response
    currentSdoResponse = getSdoResponse()

By default, this method will print the result out to the terminal. However, you can disable terminal printing by passing the optional parameter 'doPrint' and settting it false.

    # Create a new ACReader object with a (pre-defined) bus
    myReader = ACReader(bus)

    # Get the response but do not print to terminal
    currentSdoResponse = getSdoResponse(doPrint=False)