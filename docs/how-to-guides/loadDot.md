**Load A New DOT File**

Loading a new DOT file into the instance is very quick and can be saved to local data dictionaries for easier storage / parsing.

First, initialize a dotParse() class.

    myDotParser = dotParse()

Next, call the parseNewDOT() method on a file path to the DOT file.

    myDotParser = dotParse()
    myDotParser.parseNewDOT('my/DOT/path.xlsx')

Finally, you can optionally save the parsed DOT into local dictionaries for easier parsing / storage (recommended).

    myDotParser = dotParse()
    myDotParser.parseNewDOT('my/DOT/path.xlsx')
    myDotParser.dumpDictionaries()

Now, all DOT data will be saved to the /dictionaries folder. It will also stay loaded in the instance for as longas the myDotParser thread is alive, but can easily be loaded into a new instance.