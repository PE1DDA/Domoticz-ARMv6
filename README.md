# Domoticz-ARMv6
compiled domoticz for ARMv6 boards like raspberry pi B and zero(w)
install Domoticz with: sudo bash -c "$(curl -sSfL https://install.domoticz.com)" This will be the version for ARMv7!!!!!

now go to your installation directory "domoticz" with for example FileZilla and replace the file there with this one
Now on your RPI do: cd domoticz and sudo ./domoticz
Domoticz now will run
Go to your webinterface and login
Go to settings -> settings -> backup/restore
hit database restore and point to the domoticz.db from this repository, wait untill the dashboard pops up and you should be good to go!
