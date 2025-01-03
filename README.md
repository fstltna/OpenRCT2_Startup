# OpenRCT2 Startup Scripts (1.0.0)
Startup scripts for the OpenRCT2 game server - uses the "screen" command to manage session. This also restarts the OpenRTC2 process if it crashes.


---
These start up the OpenRCT2 server at boot time with a "screen" process.

1. Copy **openrct2** into **/home/openrct-user/bin** - make sure it is executable
2. Copy **startopenrct2** into **/home/openrct-user/OpenRCT2** - make sure it is executable
3. Add this to the crontab:

    @reboot /home/openrct-user/bin/openrct2 start


When you want to view the OpenRCT2 console, just enter "**screen -r**" in your shell.

To disconnect from the OpenRCT2 console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on Ubuntu 24.04 server...

If you want to turn off the server respawning type "**touch /home/openrct-user/OpenRCT2/nostart**". To reenable it type "**rm /home/openrct-user/OpenRCT2/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
