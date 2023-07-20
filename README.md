# RaspberryPi

What did I learn using Raspberry Pi zero 2 W - (Not sure how I want to form that yet also all is RAW with all kinds of errors)

Difficulties:
- I didn’t have a mouse or keyboard since the Raspberry Pi Zero 2 W has only one USB OTG port. However, this wasn’t a big problem since I only needed it for Ubuntu Server.
  + it has Bluetooth with RaspberryOS installed. (I was able to log in through SSH and connect my keyboard with trackpad by switching to bluetoothctl and running ‘scan on’ followed by ‘connect [mac address]’.)
- I have only two working micro SD cards - one of them 4GB other 16GB (on 16GB I have installed RaspberryOS)
  + (manage to install Ubuntu-server but have problems running spring boot applications - I was running out of space - $sudo apt clean fix the issue temporarly)
- My jar have't been correctly generated - (VS Code didn't show any error - I was using arrow on the left menu "Export jar..." that was a mistake, wasted a lot of time because of that )
- ./mvnw package - that the correct way of creating jar foe me - (./mvnw package -DskipTests - only if because I didn't look at tests)
-  

What I learn:
- connect to Rasberry - ssh [user]@ip
- transfer file scp [file] [user]@ip:~/
- $mv - for moving file
- $mkdir - for creating directory
- $nano - for editing file
- $sudo apt upgrade - update evrything
- $sudo apt install openjdk-17-jre-headless - to install java 17
- $sudo java -jar [filename.jar] & - to start jar file & to keep it running
- create service to run the jar when Raspberry will be restarted
  - mytest.service have to be in /etc/systemd/system
  - inside file
    - [Unit]
    - [Service]
    - [Install]
- sudo systemctl daemon-reload
- sudo systemctl enable mytest.service
- sudo systemctl start mytest.service
- sudo systemctl status mytest.service
  
- $top - use of CPU
- $df -h - use of space
- 
![ssh service status](/images/ssh_status.png "Service status")
- systemctl status mytest - to check status of my service
