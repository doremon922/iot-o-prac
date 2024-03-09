# iot-o-prac

Practical No 1
Aim: Preparing Raspberry Pi: Hardware preparation and Installation.
Requirement:
1. Raspberry Pi 3
2. Monitor or TV:A monitor or TV is connected with HDMI cable with Raspberry Pi.
3. HDMI cable(High Definition Multimedia Interface)
4. Ethernet Cable: Ethernet cable will allow Pi to connect with the Internet.
5. USB keyboard: Any standard USB keyboard and mouse can be attached to Raspberry Pi.
6. USB Mouse: This is used to connect a mouse with Raspberry Pi kit.
7. Micro USB Power supply:We can use 5v, 2A power supply for all models of Raspberry Pi.
8. 8GB or larger microSD card: SD card is used to store the default OS, Raspbian.
Installation Steps:
1.DownloadRaspbian Pi OS with zip format.
Unzip with an unzip tool.After unzipping the file, you will get a disc image (ISO.img)file in the
unzipped folder.
2.Now format the SD card before writing the disc image file on the SD card using any disk
formatter.
3.The image file of the Operating System can be written on the SD card with a Disk Imager
tool(win32 Disk Imager tool)
Plugging on the Raspberry Pi
1.Begin by placing your SD card into the SD card slot on the Raspberry Pi.
2.Plug your keyboard and mouse into the USB ports into the Raspberry pi.
3.Connect your monitor to raspberry pi with the HDMI cord.
4.With all hardwares properly attached with raspberry pi ,connect the micro USB power supply
ON and boot your computer.
Conclusion: Hence, we have successfully prepared and installed a raspberry pi kit.




Practical No 2
Aim: GPIO: Light the LED with Python without a button using Raspberry Pi.
Requirement:
1. USB Mouser
2. USB keyboard
3. Breadboard
4. LED
5. Register
6. 2 M-F Jumper wire
7. Monitor/ TV
8. Micro USB power connector
9. Display port
10. Python IDLE
Steps:
1. Set up your raspberry pi kit and connect the register and LED using a
breadboard with the help of M - F jumper wire to the raspberry pi kit.
2. Open Command editor and execute following commands (if IDLE in
not installed in raspberry pi kit)
→ sudo apt-get update
→ sudo apt-get install IDLE
3. Install GPIO package in raspberry pi kit
Open terminal and execute the following command
→ sudo apt-get install RPi.GPIO
4. Start your computer and click o cherry ICON → Go to programming
→ Go to python IDLE → select new script → write the following code
Code: Blinking LED ( add this code with above code)
import RPi.GPIO as GPIO
from time import sleep
GPIO.setwarnings(False) GPIO.setmode(GPIO.BOARD)
GPIO.setup(8, GPIO.OUT, initial=GPIO.LOW)
while True:
GPIO.output(8, GPIO.HIGH)
sleep(1)
GPIO.output(8, GPIO.LOW)
Conclusion: Hence, we have successfully performed the blinking of LED
using python code.


Practical No 3
AIM:SPI: Camera Connection and capturing Images/Videos using SPI.
Requirements:
1. USB Mouser
2. USB keyboard
3. Monitor/ TV
4. Micro USB power connector
5. Display port
6. Camera SPI
Steps: Connect the Pi camera with the raspberry pi .
Configure the camera either
1) by setting through Linux command environment
→ sudo raspi-config
2)Interface option→ Camera option 🡪Click YES→ ok-🡪Reboot Raspberry Pi to accept the
configuration
After interfacing camera
1)You can capture an image by just typing a single line command.Open terminal
windows and type the command as follows:
$ sudo raspistill –o/home/pi/Desktop/image.jpg
This command will capture an image and store it at the specified location(here the
location specified is /home/pi/Desktop)with the specified name(here the name
is’image.jpg’).
2)You can even write a code In Python to capture an image using a raspberry pi camera.
Connection :
Connect the SPI cable to the camera & IOT of the camera module properly
Conclusion: Hence we have successfully connected the camera on RPi



Practical no 4
Aim: Interface with any sensor and send its value over the internet to the server using any
suitable protocol
Hardware Requirement :
Hardware Requirements:
1. Raspberry Pi Kit.
2.HDMI cable.
3.SD Card
4.USB Mouse and Keyboard.
5.USB Micro Power Supply
6.Monitor
7.Ethernet.
Software Requirement: APACHE
Connection:
1. Plug in Ethernet cable to Raspberry Pi.
2.Install apache as follows:
a. Open Linux terminal
b. sudo apt-get update
c. sudo apt-get install apache2 -y
3.Fetch the ip address of Raspberry Pi as follows:
a. Linux Terminal --> $sudo ifconfig (press ENTER)
4.Copy the ip address and Paste in Chrome Browser ENTER --> Display the default homepage
of the apache server.
5. Change the default web page:
a. Default Page available in /var/www/html/index.html
b. Go to the following directory.
cd /var/www/html Linux terminal
c. To view the page
~$ ls
index.html
d. Since the default page(index.html) is not allowed to edit so, its ownership has to be
changed as = sudo chown pi: index.html
e. Open the page "index.html" in Python IDLE .
f. Make the changes and view in the browser.
g.index.html:
<html>
<head>
<title> Practical web server </title>
</head>
<body bgcolor="red">
<h1>Welcome to practical no. 6 </h1>
</body>
</html>
Conclusion: Hence we have successfully performed the Interface with any sensor and send its
value over the internet to the server using any suitable protocol.



Practical no 5
Aim: Node RED: Connect LED to Internet of Things
Hardware Requirements :
1. USB Mouse
2. USB keyboard
3. Breadboard
4. LED
5. Register
6. 2 M-F Jumper wire
7. Monitor/ TV
8. Micro USB power connector
9. Display port
Wiring up the circuit:
1. Connect the raspberry pi to the internet by connecting Ethernet cable to the Ethernet port or by
connecting the on board WIFI module to the router.
2. 2. Wire up the LED to any GPIO pin (i.e GPIO 8, Physical pin6) on your Raspberry Pi.
3.Star Raspberry Pi 🡪 Click on Raspberry Pi icon --> Programming menu 🡪 Click Node RED.
4. Go to Browser and type localhost:1880 and press enter.
5. Start the new flow in Node Red. (Click on ‘+’ icon)
6. Drag and drop 2 Inject buttons in the flow and one rpi gpio out button in the flow.
7. Double click on the timestamp1 and change the payload → go to the dropdown list and select
type as string and input value 1 and name of the button as “ON”.
8. Double click on the timestamp2 and change the payload → go to the dropdown list and select
type as string and input value 0 and name of the button as “OFF”.
9. Doble Click on the PIN button and select GPIO pin no 8.
10. Connect both the input and output to the PIN and deploy.
11. Prepare the bread board connection : connect led and register on breadboard.
12. Connect one jumper wire from led to GPIO pin no 6 and register on GPIO pin no 8.
13. Check the status of the LED by pressing the ON/OFF button.
9.Even the status of LED can be controlled from other computers of your network by pasting the
same address of Node RED.
Conclusion: Hence we have successfully performed Node RED: Connect LED to Internet of
Things.


Practical no 6
Aim-linux command:Exploring the raspbian
FILESYSTEM:
LS: The ls command list the content of the current directory(or one that is specified).It can be
used with the –l flag to display additional information(permissions,owner,group,size,date and
timestamp of last edit) about each file and directory in a list format.The–a flag allows you to
view files beginning with.(i.edotfiles)
CD: Using cd changes the current directory to the one specified.You can use
relative(i.ecddirectoryA) or absolute(i.ecd/home/pi/directoryA) paths.
PWD: The pwd command displays the name of the present working directory:on a Raspbian Pi,
entering pwd will output somthing like /home/pi.
MKDIR: You can use mkdir to create a new directory,e.g. mkdirnewDir would create the
directory newDir in the present working directory.
RMDIR: To remove empty directories,usermdir.So,forexample,rmdiroldDir will remove the
directory oldDir only if it is empty
CAT: You can use cat to list contents of files(s),e.gcatthisFile will display the content of
thisFile.Can be used to list the contents of multiple files,i.ecat*.txt will list the contents of all .txt
files in the current directory
HEAD: The headcommand displays the beginning of a file. Can be used with –n to specify the
number of lines to show (by default ten), or with –c to specify the number of bytes
TAIL: The opposite of head, tail displays the end of a file. The starting point in the file can be
specified either through –b for 512 byte blocks, -c for bytes, or –n for number of lines.
CHOWN: The chown command changes the user and/or group that owns a file. It normally
needs to be run as root using sudoeg. sudochownpi:root *filename* will change the owner to pi
and the group to root.
Conclusion: Hence we have successfully executed the ubuntu commands on raspbian OS.
