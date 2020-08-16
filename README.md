# DeployingSentimentAnalyser

This project deploys a basic sentiment analyser using docker and kubernetes. Emphasis will be more on kubernetes

This application has three microservices 

1) FrontEnd - ReactJS
2) Webapp Server - Java/Spring
3) Logic - Python/Flask

Docker Run commands:

1) docker run -d -p 5050:5000 chaitu0406/sentiment-analysis-logic
2) docker inspect <logic-container>
3) docker run -d -p 8080:8080 -e SA_LOGIC_API_URL="http://172.17.0.3:5000" chaitu0406/sentiment-analysis-web-app
4) docker run -d -p 8888:80 chaitu0406/sentiment-analysis-frontend

Open localhost:8888 and you should be able to access and play the application

Important Kubernetes commands
minikube start
minikube service <service-name> - info abt the service
minikube service list - List all services
kubectl apply -f <path to maifest file>
kubectl delete deployment <deployment-name>
kubectl delete service <service-name>
kubectl get all
kubectl get deployments
kubectl get pods
kubectl get svc
kubectl get nodes
minikube stop


Installation Links:
https://phoenixnap.com/kb/install-node-js-npm-on-windows (NodeJS and npm)
(Java missing)
https://mkyong.com/maven/how-to-install-maven-in-windows/ (Maven)
https://www.nginx.com/resources/wiki/start/topics/tutorials/install/ (nginx)
https://medium.com/@JockDaRock/minikube-on-windows-10-with-hyper-v-6ef0f4dc158c (minikube and kubectl)