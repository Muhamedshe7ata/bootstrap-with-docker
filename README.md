# bootstrap-with-docker
How to bind Mountaing your app*bootstrap with docker:
1- Go to :
https://startbootstrap.com/themes

2-download : SB Admin 2 - Free Bootstrap Admin Theme - Start Bootstrap
3-
 Run :
docker container run -d --name nginx_dashboard -p 8080:80 -v ${pwd}:/usr/share/nginx/html nginx
On chat Gpt:
To mount a Bootstrap website with Docker, you need to perform the following steps:
1.	Create a Dockerfile to define the base image, copy the website files to the image, and specify the default command to run when a container is created from the image.
2.	Build the Docker image using the Dockerfile.
3.	Run a container from the image and map the container's port to a port on the host machine.
Here's an example Dockerfile that could be used to mount a Bootstrap website:
# Use the official Nginx image as the base image
FROM nginx

# Copy the website files to the image
COPY . /usr/share/nginx/html

# Set the default command to run when a container is created from the image
CMD ["nginx", "-g", "daemon off;"]

You can run a container from the image using the following command:
docker run -p 80:80 my-bootstrap-website
This maps port 80 on the host machine to port 80 in the container, so that you can access the website by navigating to http://localhost in a web browser.
Source:
https://chat.openai.com/
you can also watch :
(12) Using Bind Mounting in Docker | Part 16 | Docker شرح - YouTube
https://www.youtube.com/watch?v=5ypICTcqt3Y&list=PLX1bW_GeBRhDkTf_jbdvBbkHs2LCWVeXZ&index=19&ab_channel=Codographia

