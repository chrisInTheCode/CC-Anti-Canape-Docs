**Get SDO Index**

SDO parameters can be referred to by hex index, decimal index, or parameter name. When parameters are sent over a CAN message to the VCM, their index is sent in Little-Endian-Formatted Hex (along with the rest of their payload and other attributes). However, it is not always efficient to refer to a parameter by the hex index, nor is it efficient to always convert manually between Big Endian and Little Endian. 

The dotParse class provides easy lookup methods to convert between hex indices, decimal indices, and parameter names. To start, create a new dotParse instance.

    myDotParser = dotParse()

Then, load it from either a new dot file or saved dictionaries.

    ### EITHER ###
    myDotParser.parseNewDot('my/DOT/path.xlsx')

    ### OR ###
    myDotParser.loadDictionaries()

From there, you can use any of six methods to convert between various parameter references. 

To convert from parameter name to hex index:

    newHexIndex = myDotParser.getHexIdFromParameterName(parameterName)

To convert from parameter name to decimal index:

    newDecimalIndex = myDotParser.getDecIdFromParameterName(parameterName)

To convert from decimal index to hex index:

    newHexIndex = myDotParser.getHexIdFromDecId(decimalIndex)

To convert from decimal index to parameter name:

    newParameterName = myDotParser.getParameterNameFromDecId(decimalIndex)

To convert from hex index to decimal index:

    newDecimalIndex = myDotParser.getDecIdFromHexId(hexIndex)

To convert from hex index to parameter name:

    newParameterName = myDotParser.getParameterNameFromHexId(hexIndex)

You can effectively use these methods for quick lookup and conversion between different types of parameter references.