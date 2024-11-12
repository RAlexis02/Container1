# Container1
Container1 Project - Simple Addition Web Application
This project, Container1, is a containerized web application that allows users to input two numbers and get the sum as output. It’s designed to demonstrate the basics of running a project using Docker, with a simple web interface for adding numbers.

Project Description
Container1 is a lightweight web application that takes two numbers as input, calculates their sum, and displays the result on a webpage. The application runs on a web server inside a Docker container, making it easy to deploy and run on any system that supports Docker.

Requirements
To run this project, you need the following:

Docker installed on your machine. Docker is a platform that allows applications to run in isolated containers. You can download and install Docker from Docker’s official website: https://www.docker.com/products/docker-desktop/
Checking Docker Installation
After installing Docker, confirm that it is correctly set up by running the following command in your terminal or command prompt:

bash
Copiar código
docker --version
You should see the Docker version displayed. If it’s not installed correctly, please follow the installation instructions on Docker’s official site.

Getting Started
Follow these steps to download and run the project on your local machine.

Step 1: Download the Docker Image from Docker Hub
This project is available as a pre-built image on Docker Hub, a popular repository for sharing container images. To download the image, open a terminal or command prompt and run the following command:

bash
Copiar código
docker pull rommela462/container1
This command will pull (download) the Container1 image from Docker Hub to your local Docker environment. Docker Hub hosts images that you can download and run, simplifying the process of getting this project up and running.

Step 2: Run the Container
Once the image has been downloaded, you can start the container using this command:

bash
Copiar código
docker run -d -p 8080:80 rommela462/container1
Explanation of the command:

docker run starts a new container.
-d runs the container in detached mode (in the background).
-p 8080:80 maps port 8080 on your local machine to port 80 inside the container, where the web server is running.
After running this command, the application will be accessible in your web browser at http://localhost:8080.

Step 3: Using the Web Application
Open your web browser and go to http://localhost:8080.
You will see a simple webpage where you can input two numbers.
Enter the two numbers you want to add, and click the "Add" button. The result of the addition will be displayed on the page.
Step 4: Verify the Container is Running
To confirm that the container is running, you can list all active containers with the following command:

bash
Copiar código
docker ps
This command should display rommela462/container1 as an active container, along with its container ID, status, and other details.

Stopping the Container
When you’re finished using the application, you can stop the container by running:

bash
Copiar código
docker stop <container_id>
Replace <container_id> with the actual container ID, which you can find by running docker ps.

Cleanup: Removing the Container and Image
To remove the container and free up space after stopping it, use this command:

bash
Copiar código
docker rm <container_id>
To delete the downloaded image from your system, you can run:

bash
Copiar código
docker rmi rommela462/container1
These commands ensure that the container and image do not consume unnecessary space on your machine after you’re done using them.

Summary of Commands
Here is a summary of the main commands for running and managing this project:

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
Troubleshooting
If you encounter any issues while setting up or running the project, consider the following solutions:

Ensure Docker is installed and running properly on your machine.
Confirm that you have an active internet connection to pull images from Docker Hub.
Make sure that port 8080 is not already in use by another application on your machine.
License
This project is open-source and available under the MIT License.