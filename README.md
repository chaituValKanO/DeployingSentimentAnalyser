# DeployingSentimentAnalyser

This project deploys a basic sentiment analyser using docker and kubernetes. Emphasis will be more on kubernetes


Docker Run commands:

1) docker run -d -p 5050:5000 chaitu0406/sentiment-analysis-logic
2) docker inspect <logic-container>
3) docker run -d -p 8080:8080 -e SA_LOGIC_API_URL="http://172.17.0.3:5000" chaitu0406/sentiment-analysis-web-app
4) docker run -d -p 8888:80 chaitu0406/sentiment-analysis-frontend

Open localhost:8888 and you should be able to access and play the application