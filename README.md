### Commands to build the integration

1. First launch an ec2 instance on AWS.

2. Run the following commands :

                sudo apt update

                sudo apt install openjdk-11-jre

                sudo java -version

3. Install Jenkins using the following commands :

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

4. Now install the following dependencies :

                sudo apt install nodejs

                sudo apt install npm

                sudo install npm

5. Run the app :

                 node app.js



# INTIGRATION USING THE DOCKER CONTAINER SO THAT APPLICATION CAN RUN IN THE BACKGROUND ALSO

 ### Follow the commands :

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

                

  
