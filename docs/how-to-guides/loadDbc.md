**Load A New DBC File**

Loading a new DBC file into the instance is very quick and can be saved to local data dictionaries for easier storage / parsing.

First, initialize a dbcParse() class.

    myDbcParser = dbcParse()

Next, call the parseNewDbc() method on a file path to the DBC file.

    myDbcParser = dbcParse()
    myDbcParser.parseNewDBC('my/DBC/path.dbc')

Finally, you can optionally save the parsed DBC into local dictionaries for easier parsing / storage (recommended).

    myDbcParser = dbcParse()
    myDbcParser.parseNewDBC('my/DBC/path.dbc')
    myDbcParser.dumpDictionaries()

Now, all DBC data will be saved to the /dictionaries folder. It will also stay loaded in the instance for as longas the myDbcParser thread is alive, but can easily be loaded into a new instance.