**Writing SDO Parameters**

The ACWriter class provides a convenience method for writing SDO parameter values over CAN. Start by creating a new ACWriter instance.

    myWriter = ACWriter(bus)

You will then need to create a new dotParse object.

    myDotParser = dotParse()
    
Next, load the dotParse instance from either a new dot file or saved dictionaries.

    ### EITHER ###
    myDotParser.parseNewDot('my/DOT/path.xlsx')

    ### OR ###
    myDotParser.loadDictionaries()

Then, load the dotParse object into the writer object.

    myWriter.loadDotParser(myDotParser)

You can then write a SDO Message with the singleSdoWrite() method. It requires a parameter index (can be hex index, decimal index, or parameter name) along with the payload you wish to send on the message (which can be between 0-8 bits long).

    myWriter.singleSdoWrite(parameterIndex, payload)

By default, all messages have a sub-index of 00. If a message ever needs a different sub-index, you can call the method with an optional subId argument.

    myWriter.singleSdoWrite(parameterIndex, payload, subId=??)

The method will return a value of True if no exception is thrown, else it will throw the exception. This can be used and/or modified in a variety of ways to identify that a message was concatenated correctly. However, to confirm a writing confirmation, you must get the next available SDO response message. For more information on this, see [Get SDO Response Message](./gettingSdoResponse.md)