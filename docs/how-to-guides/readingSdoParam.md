**Reading SDO Parameters**

The ACReader provides a convenience method for reading SDO parameter values over CAN. Start by creating a new ACReader instance.

    myReader = ACReader(bus)

You will then need to create a new dotParse object.

    myDotParser = dotParse()
    
Next, load the dotParse instance from either a new dot file or saved dictionaries.

    ### EITHER ###
    myDotParser.parseNewDot('my/DOT/path.xlsx')

    ### OR ###
    myDotParser.loadDictionaries()

Then, load the dotParse object into the reader object.

    myReader.loadDotParser(myDotParser)

You can then call for a SDO parameter value read command with the singleSdoRead() method. It requires a parameter index (can be hex index, decimal index, or parameter name). 

    myReader.singleSdoRead(parameterIndex)

By default, all messages have a sub-index of 00. If a message ever needs a different sub-index, you can call the method with an optional subId argument.

    myReader.singleSdoRead(parameterIndex, subId=??)

The method will return a value of True if no exception is thrown, else it will throw the exception. This can be used and/or modified in a variety of ways to identify that a message was concatenated correctly. However, to get the actual value of the parameter, you must get the next available SDO response message. For more information on this, see [Get SDO Response Message](./gettingSdoResponse.md)