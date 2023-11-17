**Reading CAN Messages**

Anti-Canape provides six different methods for different styles / implementations of reading CAN messages. For all of them, the first step is to define a ACReader class.

    reader = ACReader(bus)

1) singleCanScanOnBus() returns the next available message in the message buffer.

    reader = ACReader(bus)
    nextMessage = reader.singleCanScanOnBus()

2) singleCanScanOnID() returns the next available message in the message buffer with the specified ID.

    reader = ACReader(bus)
    nextMessageWithMyID = reader.singleCanScanOnID(myCoolIdAsAnInteger)

3) singleCanScanOnIDSet() returns the next available message in the message buffer with any of the specified ID's.

    reader = ACReader(bus)
    nextMessageWithOneOfMyIDs = reader.singleCanScanOnIDSet([myCoolIdOne, myCoolIdTwo, ...])

4) continualCanScanOnBus() continually prints off the message buffer to the terminal. It also returns a list of all message objects.

    reader = ACReader(bus)
    loggedBufferMessages = reader.continualCanScanOnBus()

    ### Terminal Printout ###

    message n data
    message n-1 data
    message n-2 data
    ...
    message 1 data

5) continualCanScanOnID() continually prints off the next message in the buffer with the specified ID to the terminal. It also returns a list of all message objects.

    reader = ACReader(bus)
    loggedBufferMessagesWithMyId = reader.continualCanScanOnId(ID)

    ### Terminal Printout ###

    message n data for id ID
    message n-1 data for id ID
    message n-2 data for id ID
    ...
    message 1 data for id ID

6) continualCanScanOnIDSet() continually prints off the next message in the buffer with any of the specified ID's to the terminal. It also returns a list of all message objects.

    reader = ACReader(bus)
    loggedBufferMessagesWithMyIdSet = reader.continualCanScanOnIdSet([ID1, ID2, ...])

    ### Terminal Printout ###

    message n data for any ID in [ID1, ID2, ...]
    message n-1 data for any ID in [ID1, ID2, ...]
    message n-2 data for any ID in [ID1, ID2, ...]
    ...
    message 1 data for any ID in [ID1, ID2, ...]