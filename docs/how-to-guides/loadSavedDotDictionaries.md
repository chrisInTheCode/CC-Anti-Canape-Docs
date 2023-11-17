**Load Saved DOT Dictionaries**

Loading saved DOT dictionaries is extremely fast and efficient. Note that you must have previously loaded a DOT file and dumped the data to the dictionaries.

First, initialize a dotParse() class.

    myDotParser = dotParse()

Then, simply call the loadDictionaries() method.

    myDotParser = dotParse()
    myDotParser.loadDictionaries()

Now, all DOT data should be loaded into the instance for easy lookup.