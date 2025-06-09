pipeline { 
    agent any 
    tools { 
        maven 'Maven' // Ensure this matches your Maven tool configuration name
    } 
    stages { 
        stage('Checkout') {  
            steps { 
                git branch: 'main', url: 'https://github.com/Darshantalawar/hello.git'  
            } 
        } 
        stage('Build') {  
            steps { 
                sh 'mvn clean package'  
            } 
        } 
        stage('Test') {  
            steps { 
                sh 'mvn test'  
            } 
        } 
        stage('Run Application') {
            steps {
                sh 'java -jar target/helllo-0.0.1-SNAPSHOT.jar'
            }
        }
    }
}

