﻿# Minikube-Local-Testing

1. Create HTML file
2. Create docker file
3. Build docker image   -  ' docker build -t image1  .'
4. Start minikube
5. Deploy the website to minikube(YAML file) -                        ' kubectl apply -f deployment.yaml '
6. Expose the website -                                                                 ' kubectl apply -f service.yaml '
7. Access the website using IP -                                                  ' minikube ip '
 

* Instead of using yaml files, we can do that manually by running 'docker run -d -p 8080:80 imageName'.
* When we change the website, after that need to build image again and stop the existing docker container if it is running. ('docker stop container_id'). Then run 'docker run -d -p 8080:80 imageName' again. Then refresh the browser to see the update of the website.

  - minikube ip - doesn't work
    
          1. Run ' minikube service list ' command
          2. Then choose website-service name
          3. Finally run ' minikube service website-service'
