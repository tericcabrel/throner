## Throner
Web application to control a drone remotely 

## Description
I work on this project with a friend. He built a drone using Raspberry Pi 3 Model combined with Arduino. He added some modules to enhance it like: 

* Camera Module of 5Mpx connected to Raspberry Pi via USB port
* GPS Module to retrieve GPS coordinates at specific time
* Portable battery to have possibility to use it without required to plug on alimentation. The battery has a lifetime of 15 minutes.
* Six servo motor to have possibility to fly
* A controller to control the drone by sending command to execute a specific action. The controller use radio frequence to send the commands.

He alse wanted to control the drone remotely through a web interface but he didn't know a lot in programming so i join him to implement this part. We was really proud of the result at the end. 


## Features
From the web interface, we will able to do the following action:

* **View battery status:** Frequently receive update of the battery life when the drone is turned on
* **Stream the camera:** We can view in realtime what the camera is focused on. 
* **Take picture:** Press a button to send command to the drone to take a picture.
* **View picture taken with the camera**: Fetch pictures taken by the camera from Throner API and display on the page
* **Controls:** A interface contains a controller with many button. When we press on one button, a command is sent to the drone to execute the action.
* **View the path:** We can access to all the sessions of the drone and for each session, we can view the path on Google Maps. <br> A session reprensent the duration between the turn on and the turn off of the drone.

## Prerequisites
* Node.js 8+
* Python 3
* RabbitMQ
* MongoDB
	
## Projects
I used 4 projects make all these features work. I will list them below and describe the role.

* **Thoner IOT:** Node.js app hosted in Raspberry Pi who communicates with client web application

* **Throner API:** REST API with Node.js and MongoDB to manage data for Throner project 

* **Throner WEB:** Web application built with React and CoreUI who allows to control a drone 

* **Throner Dispatcher:** Dispatch request between throner-api, throner-iot and throner-web 


## Screenshots