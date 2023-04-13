
# Why should I use Docker 🐳 ?

Have you ever faced this problem? 😱

> Your code works fine on your dev environment, but when you publish it on the server, it breaks and gives you errors. You don't know why and you have to fix it quickly. You find out that you forgot to install a dependency or you used a different version of a tool.

If yes, then you need Docker! 🙌

Docker is a tool that lets you create and run **containers**. Containers are like boxes that have everything your app needs to run. They have the same files, programs, and settings on any environment. You can use the same container on your dev environment, your server, or any other computer. 📦

Using Docker will make your life easier because: 😊

- You won't have to worry about missing or mismatched dependencies on your server. Your container will have them all.
- You won't have to install or configure anything on your dev environment. You can just use a container that has everything ready for you.
- You can use containers for old or new projects. You can keep the dependencies that you need without affecting other projects or systems.
- You can use containers to run your app on the cloud. You can also use tools like Docker Swarm or Kubernetes to manage multiple containers.

Docker is awesome and you should try it! 🚀


## 🐳 **Then what is Docker?** 🐳
Docker is a software platform that lets you run applications inside containers. Think of containers like virtual machines, but lighter and more efficient! 🚀

### So we use docker for : 
- Simplifies application deployment: Package your application and all its dependencies into a container that can run on any machine with Docker installed. 📦
- Increases portability: Move Docker containers easily from one environment to another, like from a developer's laptop to a production server. 🚚
- Improves scalability: Quickly spin up multiple instances of your application to handle increased traffic. 🔝

## **How does Docker work?** 🔧
Docker creates containers, which are isolated environments with their own filesystem, network, and processes. Each container runs a specific application along with its dependencies. 📁

To create a container, you first need to create a Docker image, which is a snapshot of your application and its dependencies. You can create an image by writing a Dockerfile, a script that specifies the instructions for building the image. 📜

Once you have an image, you can use it to create a container by running the `docker run` command. This starts a new container based on the image and runs the application inside it. 🏃‍♂️

### **Example of Docker in action** 💻
Let's say you have a web application that uses Node.js and MongoDB. Normally, you would need to install Node.js and MongoDB on your server and configure them to work together. With Docker, you can create two separate containers, one for Node.js and one for MongoDB, and run them on the same server

To do this, you would create two Docker images: one for the Node.js application and one for the MongoDB database. Then you would use the docker run command to start both containers, making sure to link them together so that the Node.js container can communicate with the MongoDB container.

By using Docker, you can simplify the deployment of your web application, make it more portable, and improve its scalability.

### How to install Docker 🐳

1. To get started, open this website: https://docs.docker.com/ and click on the **_Download and Install_** button. Then select the **_Docker Desktop for Windows_** or **_Docker Desktop for Mac_** or **_Docker Desktop for Linux_** button depending on your operating system. This will take you to the download page. 🖱️
2. Follow the instructions to install Docker Desktop for your operating system. You may need to restart your computer after the installation. 🔄
3. Once you have installed Docker Desktop, you will see an interface like this: 🖥️

![image](https://user-images.githubusercontent.com/97989643/231662759-9ed07c47-6066-4da4-9154-837c5861880c.png)

4. Now you can sign in to your Docker account or create a new one if you don't have one already. 🔑
5. On the interface, you will notice three sections: **_Containers_**, **_Images_** and **_Volumes_**. These are the main components of Docker that you need to know about. 📦


## **Containers , Images and Volumes** 📦

- **Containers** are like boxes that you can put things in. Each box has its own things that are separate from the other boxes. You can open and close a box without affecting the other boxes or the room. Containers are like boxes that have their own files, programs, and settings that are separate from the other containers or the computer. You can create and delete containers without affecting the other containers or the computer. Containers are fast and easy to use because they use the same system as the computer and do not need to start a whole new system like virtual machines do.
- **Images** are like instructions for making containers. They tell you what to put in a container, such as what files, programs, and settings. You can use an existing instruction from a public place like Docker Hub, or you can make your own instruction using a Dockerfile. Images do not change once they are made. You can use the same image to make many containers with the same things.
- **Volumes** are like external drives that you can connect to your containers. They let you save data that your containers make or use, such as databases, logs, or configuration files. Volumes do not get deleted when you delete a container. You can also share volumes among many containers or access them from the computer. Volumes are the best way to save data with Docker because they are easier to back up, move, and manage than other ways of saving data.
