###  Level: Beginner
  
In this Scenario, you will deploy your first NGINX API Gateway application and then you will perform logging operations. 

The Docker Container Runtime application can run Container Package-converted applications with its own application engine and facilitate deployment operations. In the coding world, large projects developed by open source software teams are also being turned into Docker Images and turned into products through the push-to-deploy concept. In our scenario, we will write a Request Router (API Gateway) that can be accessed from the outside world and redirect incoming requests from the outside world to our internal services, and turn this service into a service using simple Docker commands. Then we will keep logs of this service.

#### Instructions

To serve our applications, we need to perform the following steps in order.    

- Our Docker service is up and running. Now, use the command ``docker run --name bb-nginx -d -p 8080:80 nginx:1.22.0-alpine`` to start our Docker Container Image "[Docker NGINX Image](https://hub.docker.com/_/nginx)" 

- Congratulations, you have started your first NGINX application! Now, use the command ``docker ps`` to check the status of the running application.  

- If you can view the application with the name "bb-nginx" in the list, it means you have successfully started the application and made it available for service.  

- But let's say that page does not appear, why is my Container not working? To find out, you can see all the logs using the ``docker logs bb-nginx`` command.  

- Of course there is no error in our container and it works fine. However, there is a lot of output. Use the command ``docker logs bb-nginx --tail 5`` you can see the last 5 lines from the logs.  

- Or maybe you think something went wrong an hour ago, by using ``docker logs bb-nginx --until=60m`` command you can see logs of last 1 hour.  

- To access the running application, click the "Access Server" button above and enter the port number "8080" to access your service.  

- Congratulations, you have accessed your Nginx application and deployed a HTTP web service application to the server in less than 5 minutes using Basic Docker Commands.

With this training, you ran your first Nginx application with Docker using Basic Docker Commands. You examined how HTTP Web Service applications can be run on the server side and viewed their logs.

Continue learning with new scenarios.  







