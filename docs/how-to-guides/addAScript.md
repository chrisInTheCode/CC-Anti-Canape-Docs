**Add a Script to the Script Manager**

Adding a Script to the Script Manager (In-Code) is easy. To start, simple navigate to the ScriptManager class inside of automator.py. From there, define a new method. For this example, we will call it myNewScript.

    ###############
    # SDO SCRIPTS #
    ###############
    class SdoScriptManager():

        def __init__(self, driver:str) -> None:

        ...

        def myNewScript():

Now, lets add a few arguments to the method. You are required to add 'self' as an argument so that it can use class obejcts.

    def myNewScript(self):

You can also optionally add timeDelay as an argument. This will allow you to change the wait time between each message in the SdoAutomator() class methods if you pass it along and implement those methods, although they default to having a delay of 0.03s. 

    def myNewScript(self, timeDelay=0.03):

The first step with any script / action is to open a bus to communicate with. Since the Script Manager requires you to specify the driver/dongle at instance creation, you can easily use the included getDefaultBus() method without asking for another driver/dongle. You can implement this as such:

    def myNewScript(self, timeDelay=0.03):
        myBus = getDefaultBus(self.bus)

From there, you can implement your script inside this function however you would like. You can add arguments, return values, dependencies, etc. all from within this method.

    def myNewScript(self, timeDelay=0.03):
        myBus = getDefaultBus(self.bus)

        # Implement all of your script code here
