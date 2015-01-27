# grut-IoT
The technical design for Grut can be divided into 3 parts:

1. The sensors and their connection to the database
	=> Arduino Mosquitto sketch to be installed on Arduino Yun
		This file allows the Arduino to connect to the server and send information
	=> mqtt_persist.js file to be stored on server 
		Allows server to receive information from the Arduino and store it in the database

2. The website (back-end and front-end) coded in the CakePHP framework
	These files are stored in the 'upload' folder.

	Front-end:
	=> css.style file has all css and styling of the website stored
	=> default.ctp has some of the HTML stored and all the Javascript (jQuery) and AJAX calls used
	=> View files belonging to corresponding Models and Controllers. These present the information to the screen and pass information to the Controllers.

	Back-end:
	=> Model files fetching information from the database
	=> Controller files with logic and computations on database information

3. The SQL file for the database


To get the project up and running one needs to:

- Set up database & import SQL file.
- Set up server & upload the website files to 'web' directory.
- Adapt CakePHP configurations for database.
- Configure Arduino Yun, adapt it to server being used, and upload Mosquitto sketch to it. 
- Adapt mqtt_persist file to database and server being used, and store it on the server.
- Install Mosquitto client on Arduino Yun and Mosquitto broker on machine (server)
- Make sure Yun is sending the right message and machine / server is listening to this message
- Attach sensors to Arduino, solder LED if necessary, attach it 




         
