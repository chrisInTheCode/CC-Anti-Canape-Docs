**Writing CAN Messages**

Anti-Canape provides four different methods for different styles / implementations of writing CAN messages. For all of then, the first step is to define a ACWriter class.

    writer = ACWriter(bus)

1) singleCanWriteOnID() writes a single message with a given ID and signalDict.

    writer = ACWriter(bus)
    writer.singleCanWriteOnID(ID, {signal1:value1, signal2:value2, ...})

2) singleCanWriteRawOnID() writes a single message with a given ID and raw payload (Input As Big Endian).

    writer = ACWriter(bus)
    writer.singleCanWriteRawOnID(ID, "76543210")

3) constantCanWriteOnID() continually writes the same message with a given ID and signalDict. It also takes (as arguments) a period parameter, for how long to wait between messages, and a duration parameter, for how long to keep sending messages.

    writer = ACWriter(bus)
    writer.constantCanWriteOnID(ID, {signal1:value1, signal2:value2, ...}, timeBetweenMessages, howLongToKeepSending)

4) constantCanWriteRawOnID() continually writes the same message with a given ID and payload. It also takes (as arguments) a period parameter, for how long to wait between messages, and a duration parameter, for how long to keep sending messages.

    writer = ACWriter(bus)
    writer.constantCanWriteRawOnID(ID, "76543210", timeBetweenMessages, howLongToKeepSending)