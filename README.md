# Domoticz-ARMv6

Like (many) others I got struck by updating Domoticz to the latest release at the beginning of january 2024, because I didn't read the update information
(I seldom did......... was used to just clicking that "green" button)
I'm sure that (many) others experienced the same.
Running Domoticz for many years on my Raspberry Pi zero W, after updating -> no go, so I tried a cmd-line update and an update beta with no luck.
Only after all that I read about the ceased support for ARMv6

Since I am still satisfied with my (old) RPI zero W, I started to search for solutions and the only one applicable seemed to start building from source....!
This has to be done on an ARMv6 device, so I started following the instructions from the Domoticz WiKi and compiled domoticz (13-01-2024) for ARMv6 boards from source.
This took almost 2 full days to complete on my RPI zero, also because Boost and GCC have to be installed, this all takes a lot of time to complete.

Now, here is my solution:

On a freshly installed bullseye light via the Raspberry Pi Imager (nice tool to be downloaded from RPI's site).

install Domoticz with: sudo bash -c "$(curl -sSfL https://install.domoticz.com)" 
This will be the version for ARMv7, but just install it
After installation is complete, do not reboot, but go to your installation directory "domoticz" with for example FileZilla
Replace the file "domoticz" with the one abow on this site/page
Now on your RPI do:
cd domoticz
sudo ./domoticz
Domoticz now will run
Go to your webinterface and login (user admin, pw domoticz)
Go to settings -> settings -> backup/restore
hit database restore and point to the domoticz.db from this repository, wait untill the dashboard pops up and if all went well, you
should see the dashboard with some devices from Buienradar (Dutch weather site) and a Dummy.
Ofcourse those can be deleted, but try some of your favorite apps or plugins first to see if it is fully working.
Now you are good to go
Make sure to disable Software Updates because they will be for ARMv7 systems!
