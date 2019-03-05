pipeline {
    agent any 
    stages {
       stage('Build') {
           steps {
               sh 'mvn clean package'
               sh 'sudo docker build -f example.df 
			   sh 'sudo docker container run -it -d -p 8888:8080 tomcat'
           }
       }     

    }  
}

