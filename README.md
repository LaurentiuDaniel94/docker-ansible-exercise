# docker-ansible-exercise

[Requirements]

  Create deployment scripts using Ansible to deploy an app to target servers/VM.  

  Use complete "Todo" app provided by Docker.

    → The app contsins two services: the main app and a db. 
    → Use app with the Docker-compose file config.
    → Create deploy playbook using Ansible to be able to easily deploy the "Todo" app cloud.
    → Execute the deploy job for one VM and ensure it works as expected.
    → App should work as expected in the VM.
    → You must assume that the target VM only has as basic Linux installation. Packages that are specific to the deployment of this app are not already     available and must be installed.

- In one public repo, please provide the following:
	- Ansible playbook and inventory for deploy of the app.
	- Link to VM where the app can be seen.
	- README file to facilitate navigation to VMs.


[My Solution]


1. Created three Ubuntu droplets on cloud.digitalocean.com
   -> Workstation
      -> Installed in the workstation Docker and Ansible
   -> Ubuntu-testServer-01
   -> Ubuntu-testServer-02
   
2. Cloned the repo for "Todo" app from the requirement: https://docs.docker.com/get-started/02_our_app/
   - Created the Dockerfile.
   - Pushed the final docker image to Docker Hub
   - The playbook uses community.docker.docker_container module to manage the docker image from Docker Hub.
   
3. Links to the two Ubuntu Servers:
    - http://167.99.43.204:3000 (Ubuntu-testServer-01)
    - http://167.99.43.95:3000  (Ubuntu-testServer-02)
