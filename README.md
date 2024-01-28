# FlipperUsbExfil
A BadUSB Duckyscript for the Flipper Zero that is able to exfil the captured data back onto the Flipper Zero.

# Why? 
In case you cant use online exfiltration.

# How to use?
You connect the Flipper to a Windows PC and execute your BadKB payload. After the Flipper is done *quickly* switch to the Flippers applications and select USB-> Mass Storage -> select your disc image

You know its working when the Mass Storage is being written to.

if you are slow you might want to increase the sleeping time


# How does it work?

The flipper executes the payload as usual and saves the goodies in a file.
Then the flipper uses powershell to write a powershell script and execute it.
Now the Flipper is done with inputting keystrokes and thus you can change it into being a USB drive.
While you change the Flipper, the script will wait a set amount of seconds and after that will start to write the goodiesfile onto the Drive

After that you should do some clean up (Checkout I-Am-Jakoby's Repository https://github.com/I-Am-Jakoby/PowerShell-for-Hackers for payloads and  "Clean-Exfil")
