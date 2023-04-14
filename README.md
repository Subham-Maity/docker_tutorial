
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


## **Then what is Docker?** 🐳
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
- **Images** are like recipes for making containers. They tell you what ingredients and steps you need to make a container. You can use an existing recipe from a public place like Docker Hub, or you can write your own recipe using a Dockerfile. Recipes do not change once they are written. You can use the same recipe to make many containers with the same ingredients and steps.
> let's say you have a project that consists of a web application written in Node.js, a backend server written in Java, and a machine learning component written in Python. You can create three separate Docker images for each of these components, each with its own dependencies and configurations, and then use them to create containers that can run the entire project.

> For instance, you can create a Docker image for the Node.js application by specifying the base image as node and then copying the application code into the container. You can then build and tag the image with a specific name, like my-node-app.
- **Volumes** are like external drives that you can connect to your containers. They let you save data that your containers make or use, such as databases, logs, or configuration files. Volumes do not get deleted when you delete a container. You can also share volumes among many containers or access them from the computer. Volumes are the best way to save data with Docker because they are easier to back up, move, and manage than other ways of saving data.


## **Let's start with Docker** 🔥

Sure, I can help you with that. Here is the rewritten text with bullet points changed to numbers:

```
1. First open this website for postgresql: https://hub.docker.com/_/postgres
you will see this right side of the page:
```bash
docker pull postgres
```
2. Open your terminal and type this command:
```bash
docker pull postgres
```
> - You can check docker is installed or not by typing this command: `docker --version`
> - You can visit the docker documentation for pull command: https://docs.docker.com/engine/reference/commandline/pull/
> - Pulling an image doesn't mean installing it. It just means that you are downloading the image from the Docker Hub to your computer.
> - It will download the latest version of the image. If you want to download a specific version, you can add the version number after the image name. For example, `docker pull postgres:9.6.2` will download the 9.6.2 version of the image.

3. Now may be you want to check your images, so type this command:
```bash
docker image ls
```
> - You can visit the docker documentation for image command:https://docs.docker.com/engine/reference/commandline/image/

You can see the output like this:
```bash
REPOSITORY   TAG       IMAGE ID       CREATED        SIZE
postgres     latest    ceccf204404e   30 hours ago   379MB
```
> Even you can open the docker desktop and check the images there ,and you will see the same output.
> - You can visit for ps command: https://docs.docker.com/engine/reference/commandline/ps/


4. Now if you want to run postgresql, first you should visit postgresql documentation: https://hub.docker.com/_/postgres check for `How to use this image`
- You will see this:
```bash
$ docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres
```
5. Now open your terminal you need to modify this command:
```bash
docker run -e POSTGRES_PASSWORD=mysecretpassword postgres
```
> here e is for environment variable, and POSTGRES_PASSWORD is the environment variable name, and mysecretpassword is the value of the environment variable.
now you can
> here e is for environment variable, and POSTGRES_PASSWORD is the environment variable name, and mysecretpassword is the value of the environment variable.
now you can see the output like this:
```bash
PostgreSQL init process complete; ready for start up.

2023-04-13 13:00:11.415 UTC [1] LOG:  starting PostgreSQL 15.2 (Debian 15.2-1.pgdg110+1) on x86_64-pc-linux-gnu, compiled by gcc (Debian 10.2.1-6) 10.2.1 20210110, 64-bit
2023-04-13 13:00:11.431 UTC [1] LOG:  listening on IPv4 address "0.0.0.0", port 5432
2023-04-13 13:00:11.432 UTC [1] LOG:  listening on IPv6 address "::", port 5432
2023-04-13 13:00:11.443 UTC [1] LOG:  listening on Unix socket "/var/run/postgresql/.s.PGSQL.5432"
2023-04-13 13:00:11.455 UTC [62] LOG:  database system was shut down at 2023-04-13 13:00:11 UTC
2023-04-13 13:00:11.465 UTC [1] LOG:  database system is ready to accept connections
```

> - If you want to shut down you can simply type `wsl --shutdown` in your terminal.
> - If you don’t interact with the container, it will eventually exit. However, you can keep the container running by interacting with it or by running it in detached mode using the -d flag when starting the container. For example, `docker run -d -e POSTGRES_PASSWORD=mysecretpassword postgres` will start the container in detached mode.

6. Now hit `docker run -e POSTGRES_PASSWORD=mysecretpassword -d postgres`
> One Id will be generated
7. Now if you want to check your containers on the software, you can see `the another container` is running with another name.
8. Now if you want to check your containers on the terminal, you can type this command:
```bash
docker ps
```
> you will see the output like this:
```bash
CONTAINER ID   IMAGE      COMMAND                  CREATED         STATUS         PORTS      NAMES
8fee7f681552   postgres   "docker-entrypoint.s…"   2 minutes ago   Up 2 minutes   5432/tcp   beautiful_curie
```
9. Now if you want to stop the container, you can type this command:
```bash
docker stop my_container
```
> - in my case, my_container is beautiful_curie
> - or you can go to the docker desktop and click on the stop button.
