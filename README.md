# Overview
This project was done as part of IPs at Moringa school by George Mutwiri

This project involved the containerization and deployment of a full-stack yolo application using Docker.

YOLO

Overview: IP Submission

Installation
Vagrant Setup:
Install Vagrant and VirtualBox (or another provider).

Clone the repository to your local machine.
git clone https://github.com/mgeorgey/yolo.git
cd yolo


Initialize the Vagrant environment.
vagrant up
This will set up a virtual machine with all necessary dependencies.

Docker Compose Setup
Install Docker and Docker Compose if you haven't already.

Navigate to the project directory.

cd yolo

Build and start the containers using Docker Compose.
docker-compose up --build
This will bring up the services defined in your docker-compose.yml.

Deployments
Backend Deployment
The backend deployment is configured in the backend-deployment.yml file, which contains all the configurations required to deploy the backend services.

To deploy the backend:
Ensure that the Docker containers are running.
You can modify the backend-deployment.yaml to tweak deployment settings as necessary.
Apply the deployment using the following command:
kubectl apply -f backend-deployment.yml

Frontend Deployment
The frontend is deployed separately and is configured in the frontend-deployment.yaml.
To deploy the frontend:
Make sure that your backend services are up and running.
Apply the frontend deployment YAML file:
kubectl apply -f frontend-deployment.yml

Configuration Files

Inventory
The inventory file contains configuration details for the different environments in which your project can be deployed. It includes settings for both backend and frontend components.
To modify the inventory:
Open the inventory file.
Update the relevant environment configurations (e.g., IP addresses, service names).

Playbook YAML
The playbook.yml is a key configuration file for automating the deployment process using Ansible. It defines the steps to provision the infrastructure, install dependencies, and start the services.
To use the playbook:
Install Ansible on your local machine.
Run the playbook:
ansible-playbook playbook.yml

Open your browser and navigate to http://localhost:5000.
You should see the Node.js application running.

Contributing
We welcome contributions! If you would like to contribute, please fork the repository and submit a pull request with your changes. Make sure to follow the coding style and add tests where applicable.

License
This project is licensed under the MIT License - see the LICENSE file for details.