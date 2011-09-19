Ruby reading Arduino over serial port
=====================================

The purpose of this code is for an Arduino to print over the 
serial port to a linux machine. A ruby script running on the
linux machine will print out what it receives over the serial
port.

Much of the code has come from the following:
http://www.arduino.cc/playground/Interfacing/LinuxTTY
http://www.arduino.cc/playground/Interfacing/Ruby

You will need:
- A linux machine with Ruby and Rubygems installed
- An arduino and a USB cable

Setup
-----

* Install the ruby gem serialport (you may need sudo)
	<blockquote>gem install serialport</blockquote>

* Setup the serial port (may need sudo here as well)
	<blockquote>stty -F /dev/ttyUSB0 cs8 9600 ignbrk -brkint -icrnl -imaxbel -opost -onlcr -isig -icanon -iexten -echo -echoe -echok -echoctl -echoke noflsh -ixon -crtscts</blockquote>

* Test the Serial port with 'cat' (quit by hitting <ctrl>-c)
	<blockquote>cat /dev/ttyUSB0</blockquote>

Run the code
------------

* Run the code (may need sudo)
	ruby arduino.rb

* You should see the words 'High' and 'Low' printing in the terminal

* Stop the script
	<ctrl>-c