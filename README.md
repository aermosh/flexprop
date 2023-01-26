*******************************************************************************************

Working with P2 (Parallax Propller 2) - flexprop build for Fedora 37

flexprop release:
https://github.com/totalspectrum/flexprop/releases/tag/v5.9.23

******************************************************************************************

1. Download flexprop.tar.gz and unzip it into /opt (so that it’s /opt/flexprop):

sudo tar -xvzf flexprop.tar.gz -C /opt

*****************************************************************************************

2. Create symbolic link for flexprop:

sudo ln -s /opt/flexprop/flexprop /usr/local/bin/flexprop 

or 

Use flexprop link from this repository and move it or copy using -P option to usr/local/bin

Move:

sudo mv flexprop /usr/local/bin 

Copy:

sudo cp -P flexprop /usr/local/bin

****************************************************************************************

3. Start flexprop IDE:

flexprop &

Open hello_world_flexprop.cpp then compile it and run: 
 
File -> Open -> hello_world_flexprop.cpp -> Compile & Run on P2

FlexProp ANSI Terminal Window should open with the following message:

Hello World from flexprop! 


If you see the error message in terminal window:  

Could not find a P2                                                             
                   Press enter to continue...

make sure you are a member of dialout group. Run the following command:

groups

The output of groups command could look soemthing like this:

user_name wheel dialout

If there is no dialout in the list provided by groups command add yourself to dialout group:

sudo usermod -a -G dialout user_name

You would need to logout and sign back in to see the effect of usermod command.

Also see 

https://www.parallax.com/propeller-2/get-started/flex-c/

for more more information and troubleshooting. Could not find a P2 paragraph is below:

Could not find a P2

If you get a “Could not find a P2” error message in the Propeller Output window, check and make sure that you’ve closed all other Propeller Output windows. Only one Propeller session may be open at a time, and if you try to run a program while a Propeller Output (terminal) window is open then it will not work and the P2 will not be found.

If that isn’t the problem, check the connection to your P2, and look under the Ports menu to see which port is selected. If you know which port the P2 is connected to, you may manually select that one to force FlexProp to use it.

If you have multiple P2 devices connected to your computer, you may select a specific port to connect to by finding it under the Ports menu in FlexProp. If the port you want does not show up, click on Ports > Scan for ports.
  
*******************************************************************************************

