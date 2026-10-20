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


token:
<br>
K106a34920e459390b299850fe5607e9280aea33c85c792ce0fe63b27595f1144a8::server:ea012671d97888c8c48c1b1f1525f3b4


<h2> Comanda pentru Cluster </h2>
curl -sfL https://get.k3s.io | K3S_URL="https://192.168.1.101:6443" K3S_TOKEN="TOKENUL_TAU" sh -

<h2> Verificam conectarea </h2>
sudo k3s kubectl get nodes -o wide
