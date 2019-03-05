pipeline {
    agent any 
    stages {
	       stage('Build') {
           step {
               sh 'mvn clean package'
			   }
			step {   
               sh 'sudo docker build -f ./example.df docker
			   }
			step {   
			   sh 'sudo docker container run -it -d -p 8888:8080 docker'
           }
       }     

    }  
}

