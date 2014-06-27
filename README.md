FakeMCServer
============

![Alt text](http://image-upload.de/image/fJMilM/4fe71c6994.png)

A Fake Minecraft Server, that shows the following messages:

* motd
* version
* maxplayers
* playerlist
* kickmessage

You can customize all messages. The configuration files are created automatically for you the first time you start the fake server. Compile the .jar or download the compiled version here: https://mega.co.nz/#!ad1AUCKD!IDdb8dw8hCcy_r0InkkBK58OOEEuVEv_gNGt-L__QVk

The fake server can be manually started by running the following line:

<pre>
java -jar FakeMCServer.jar -port 25565
</pre>


The minecraft init script (for linux) may be copied to /etc/init.d/ then run 'chkconfig --level 345 minecraft on' to install the service. You may then run 'service minecraft help' for a list of commands supported by this script. 'service minecraft start' will start your minecraft/bukkit/other server, and 'service minecraft stop' will give players a 15 second warning, then shutdown the server. Once the server has stopped, the fake server will automatically start to take its place. You may also create a cron by running the command 'crontab -e' then add the line below. This will check once a minute, and automatically start the fake server if neither the fake or real servers are running.

<pre>
# minecraft service
* * * * * service minecraft cron
</pre>


* You can use color codes with '&' (for example "&4I'm Red!") The full list of color codes can be found here: http://minecraft.gamepedia.com/Formatting_codes
* You can make new lines with '\n' for multiline motd, the playerlist and the kickmessage
* You can use unicode: if you want to use special charakters, the convert to JavaScript Escapes (http://rishida.net/tools/conversion/)


Have fun ;)

