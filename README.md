Container1 Project - Simple Addition Web Application
This project demonstrates a basic setup of a containerized web application for adding two numbers. It’s designed to showcase how to run a project using Docker, with a simple web interface for inputting numbers and obtaining their sum.

📋 Project Overview
Container1 is a Dockerized web application built using HTML and JavaScript. It takes two numbers as input, calculates their sum using JavaScript, and displays the result on a webpage. The application runs on a web server inside a Docker container, making it easy to deploy and run on any system that supports Docker.

🛠 Requirements
To run this project, ensure you have the following:

Docker installed on your machine. Docker allows applications to run in isolated containers. Download Docker from the official site: Docker Installation.  https://www.docker.com/products/docker-desktop/
✅ Verifying Docker Installation
Open a terminal or command prompt on your computer.

On Windows: Search for "Command Prompt" or "PowerShell" in the Start menu.
On macOS: Open "Terminal" from Applications > Utilities.
On Linux: Use your default terminal application.
In the terminal, type the following command to check if Docker is installed correctly:

bash
Copiar código
docker --version
You should see the Docker version displayed. If not, follow the installation instructions on Docker’s official website.

📂 Project Structure
The project files are organized as follows:

plaintext
Copiar código
container1_addition/
├── index.html     # Main HTML file with input fields and JavaScript code for addition
└── Dockerfile     # Docker configuration for the project
index.html: Contains the HTML and JavaScript code that allows users to input two numbers, calculate their sum using JavaScript, and display the result.
Dockerfile: Instructions for Docker to build and run the application in a container.
🚀 Getting Started
Follow these steps to download and run the project on your local machine.

Step 1: Pulling the Docker Image
This project is available as a pre-built image on Docker Hub, a repository for sharing container images.

Ensure Docker Desktop is running.

You should see the Docker icon in your taskbar or system tray. If it’s not open, find and launch Docker Desktop.
Open a terminal or command prompt on your computer.

In the terminal, type the following command to pull (download) the image:

bash
Copiar código
docker pull rommela462/container1
This command downloads the Container1 image from Docker Hub to your local Docker environment.
Step 2: Running the Container
Now that the image is downloaded, start the container with the following command:

bash
Copiar código
docker run -d -p 8080:80 rommela462/container1
Explanation of the command:

-d: Runs the container in detached mode, meaning it will run in the background.
-p 8080:80: Maps port 8080 on your local machine to port 80 inside the container, where the web server is running.
After this, you can open your web browser and go to http://localhost:8080 to use the application.

💻 Using the Web Application
Access the Application: Open a web browser and visit http://localhost:8080.
Enter Two Numbers: You will see a simple webpage where you can input two numbers.
Calculate the Sum: After entering the numbers, click the "Add" button, and the JavaScript code will calculate and display the result of the addition on the page.
🛑 Stopping the Container
When you’re finished using the application, you can stop the container to free up resources:

Identify the container ID by running:

bash
Copiar código
docker ps
Use the following command to stop the container:

bash
Copiar código
docker stop <container_id>
Replace <container_id> with the actual container ID, which you obtained in the previous step.

🧹 Cleanup
If you no longer need the container and want to free up space on your machine, follow these steps:

Remove the container (after stopping it):

bash
Copiar código
docker rm <container_id>
Remove the Docker image from your system:

bash
Copiar código
docker rmi rommela462/container1
These commands help keep your Docker environment clean and prevent unnecessary storage use.

🔄 Summary of Commands
For quick reference, here is a summary of the main commands:

bash
Copiar código
# Pull the image from Docker Hub
docker pull rommela462/container1

# Run the container
docker run -d -p 8080:80 rommela462/container1

# Check running containers
docker ps

# Stop the container
docker stop <container_id>

# Remove the container
docker rm <container_id>

# Remove the image
docker rmi rommela462/container1
💡 Troubleshooting
If you encounter issues while setting up or running the project, consider the following:

Docker Installation: Ensure Docker is installed and Docker Desktop is running.
Network Issues: Confirm that you have an active internet connection to pull images from Docker Hub.
Port Conflicts: Make sure port 8080 is not already in use by another application. If it is, you can choose a different local port (e.g., -p 8081:80) when running the container.
📜 License
This project is open-source and available under the MIT License.