Steps followed to build Docker Image push it on Docker-Hub and the create a Deployment using that image

1. First we have to docker login
    -  docker login
2. Now we build the image from the DockerFile
    -  docker build -t <image-name>:tag .
3. Push image on Docker-hub
    -  docker push <image-name>:tag
4. Create deployment
    -  kubectl create deployment <deployemnt-name> --image=<image-name>:tag
5. Expose our deployment on a port
    -  kubectl expose deployment my-webapp --type=LoadBalancer --port=3000
6. To get the access url of our app
    -  minikube service <deployment-name>
7. Now paste that URL on browser and access the application.

   ![Web-app_Op](https://github.com/user-attachments/assets/70302ffe-a4e6-443f-b028-240ab356b83d)

