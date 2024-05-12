	1. Create HTML file
	2. Create docker file
	3. Build docker image   -  ' docker build -t image1  .' 
	4. Start minikube
	5. Deploy the website to minikube(YAML file) -                        ' kubectl apply -f deployment.yaml ' 
	6. Expose the website -                                               ' kubectl apply -f service.yaml ' 
    7. Access the website using IP -                                      ' minikube ip '


    If minikube ip - doesn't work

			1. Run ' minikube service list ' command
			2. Then choose website-service name
            3. Finally run ' minikube service website-service' 