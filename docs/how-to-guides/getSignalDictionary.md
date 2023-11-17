**Get a CAN Message (Signal Dictionary)**

Looking up a CAN Message (Signal Dictionary) from an arbitration ID or signal name is extremely easy with the help of CC-dbcAutoParse.

First, create a new dbcParse() instance.

    myDbcParser = dbcParse()

Then, load it from either a new dbc file or saved dictionaries.

    ### EITHER ###
    myDbcParser.parseNewDbc('my/DBC/path.dbc')

    ### OR ###
    myDbcParser.loadDictionaries()

Finally, there are two methods that provide quick and easy message lookup. 

You can either look up by arbitration ID:

    newMessage = getMessageById(ID)

Or you can look up by one of the signal names on the message:

    newMessage = getMessageBySignalName(signalName)

Both will return the full signal dictionary of the message.