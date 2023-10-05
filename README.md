
# Hi, I'm Ravi Chandra! 👋


# Automated Todo App CI/CD with DevOps, Docker, and GitHub.This code is taken from github to implement this app using devops tools ( Docker,Jenkins,AWS) 

 Introduce my latest project, "Automated Todo App with Jenkins, Docker, and GitHub". 


## Installation

Run ec2 instance on AWS !

Install the Jenkins using the following commands :

```bash
    sudo apt update

    sudo apt install openjdk-11-jre

    sudo java -version

    curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
    /usr/share/keyrings/jenkins-keyring.asc > /dev/null

    echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
    https://pkg.jenkins.io/debian binary/ | sudo tee \
    /etc/apt/sources.list.d/jenkins.list > /dev/null

    sudo apt update

    sudo apt install jenkins

    sudo systemctl enable jenkins

    sudo systemctl start jenkins

    sudo systemctl status jenkins

```

## Run Locally

Clone the project

```bash
  git clone https://github.com/Ardnahcivar01/node-todo-app.git
```

## First you need to install the jenkins so follow the Installation commands.


Install dependencies

```bash
  sudo apt install nodejs

  sudo apt install npm

  sudo install npm
```

Start the server

```bash
   node app.js
```


## Optimizations

What optimizations did we needed at this stage ?

My Todo app is currently hosted on an EC2 instance, and it operates only as long as the server is active. If the server is stopped, the app also ceases to function. To address this, I'm in the process of encapsulating the entire codebase and application within a Docker container, achieved by creating a Dockerfile. This adjustment will enable the app to run seamlessly in the background, providing a more robust and reliable deployment solution.

# Docker Commands 

```bash
      sudo rm -rf Dockerfile

      sudo apt install docker.io
            
      sudo vi Dockerfile 

              FROM node:12.2.0-alpine
              WORKDIR app
              COPY . .
              RUN npm install
              EXPOSE 8000
              CMD ["node","app.js"]

      docker build . -t node-app

      sudo usermod -a -G docker $USER

      docker run -d --name node-todo-app -p 8000:8000 todo-node-app
```


## 🔗 Links

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ravi-chandra-5a2b99230)



## Feedback

If you have any feedback or any problem, You can mail me or can contact me on linkedin.  ravi.21jdai027@jietjodhpur.ac.in
