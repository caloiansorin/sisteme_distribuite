🐳 Sisteme Distribuite — Apache Video Server

<div align="center">
<img src="https://img.shields.io/badge/Ubuntu-WSL-E95420?logo=ubuntu&logoColor=white" alt="Ubuntu WSL">
<img src="https://img.shields.io/badge/Docker-Container-2496ED?logo=docker&logoColor=white" alt="Docker">
<img src="https://img.shields.io/badge/Apache-Web_Server-D22128?logo=apache&logoColor=white" alt="Apache">
</div>

<br>

<p align="center">
<b>Deploying an Apache Video Server using Ubuntu on WSL and Docker.</b>
</p>

📌 Overview

This project demonstrates how to deploy an Apache web server using a prebuilt Docker image on Ubuntu running under Windows Subsystem for Linux (WSL).

🛠️ Prerequisites
Windows with WSL support
Ubuntu installed through WSL
Docker installed and running
The apache-video.tar Docker image archive
🚀 Installation and Setup
1. Install WSL with Ubuntu

Run in PowerShell as Administrator:

wsl --install Ubuntu

2. Update Ubuntu

Open the Ubuntu terminal and execute:

sudo apt-get update
sudo apt-get upgrade -y

3. Load the Docker Image

Make sure apache-video.tar is accessible from your current directory.

docker load -i apache-video.tar

4. Verify the Docker Image

List the available Docker images:

docker images


Expected image:

Repository	Tag
apache-video	v1
5. Start the Apache Container

Run the following command:

docker run -d \
  --name apache-video \
  -p 8080:80 \
  apache-video:v1


Command explanation:

Option	Description
-d	Runs the container in the background
--name apache-video	Assigns a name to the container
-p 8080:80	Maps host port 8080 to container port 80
apache-video:v1	Specifies the Docker image and tag
🌐 Access the Application

Once the container is running, open your browser:

<p align="center">
<a href="http://localhost:8080">
<img src="https://img.shields.io/badge/OPEN-APACHE%20VIDEO%20SERVER-2ea44f?style=for-the-badge" alt="Open Apache Video Server">
</a>
</p>

URL: http://localhost:8080

🔍 Useful Docker Commands
Command	Description
docker ps	Display running containers
docker ps -a	Display all containers
docker images	List available images
docker logs apache-video	Display container logs
docker stop apache-video	Stop the container
docker start apache-video	Start the container
docker rm -f apache-video	Remove the container
🧰 Troubleshooting
Container is not running
docker ps -a
docker logs apache-video

Container name is already in use
docker rm -f apache-video


Then execute the docker run command again.

Application is not accessible
Verify that the container is running.
Ensure port 8080 is not being used by another application.
Check the container logs for errors.
Make sure Docker is running and properly integrated with WSL.
📁 Project Structure
sisteme_distribuite/
├── README.md
└── apache-video.tar


Note: The project structure is illustrative. The Docker image archive must be available locally.

<div align="center">
<sub>📚 Course: Sisteme Distribuite</sub>
<br>
<sub>🐳 Technologies: Ubuntu · WSL · Docker · Apache</sub>
</div>

token:
<br>
K106a34920e459390b299850fe5607e9280aea33c85c792ce0fe63b27595f1144a8::server:ea012671d97888c8c48c1b1f1525f3b4
