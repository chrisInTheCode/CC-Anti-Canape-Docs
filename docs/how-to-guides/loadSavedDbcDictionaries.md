**Load Saved DBC Dictionaries**

Loading saved DBC dictionaries is extremely fast and efficient. Note that you must have previously loaded a DBC file and dumped the data to the dictionaries.

First, initialize a dbcParse() class.

    myDbcParser = dbcParse()

Then, simply call the loadDictionaries() method.

    myDbcParser = dbcParse()
    myDbcParser.loadDictionaries()

Now, all DBC data should be loaded into the instance for easy lookup.