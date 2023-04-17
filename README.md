AWS EC2 Instance Setup || Docker Installation || SonarQube Integration with Azure DevOps

1. Connect to your EC2 instance
   Log in to your AWS Management Console
   Select EC2 from the list of services
   Connect to your Ubuntu EC2 instance using SSH.


2. Install Docker on an Ubuntu EC2 instance on AWS
   Update the package list: Run the following command to update the package list:
   - sudo su
   - apt-get update
   - apt-get upgrade

3. Run the following command to install Docker
   - apt-get install -y docker.io


4. Verify the installation: Run the following command to verify that Docker is installed correctly:
   - docker --version
    This command should display the version of Docker that was installed.

5. To setup SonarQube on Docker, you can follow these steps:
   Pull the SonarQube Docker image by running the following command in your terminal:
   - docker pull sonarqube

6. Once the image is downloaded, you can create a container and start SonarQube by running the following command:
   This command creates a Docker container named "sonarqube" with the SonarQube image, and maps the container's port 9000 to the host's port 9000.
   - docker run -d --name sonarqube -p 9000:9000 sonarqube

7. Wait for a few minutes for the SonarQube server to start. You can check the logs of the container by running the following command:
   - docker logs -f sonarqube
   - docker ps (This command can be used to display the list of running Docker containers on your local system)

8. Once the server is up and running, you can access the SonarQube web interface by opening a web browser and navigating to http://PUBLIC-IP-OF-EC2:9000

9. By default, SonarQube requires a login. The default username is "admin" and the default password is "admin". You can change these credentials in the SonarQube web interface.
