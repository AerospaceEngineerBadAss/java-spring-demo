pipeline {     
    agent any  
    tools{
        maven 'my_maven'
    }
        stages {          
            stage('Checkout') {
                    steps {                    
                        git branch: 'main', url: 'https://github.com/AerospaceEngineerBadAss/java-spring-demo'          
                    }          
            }          
            stage('Build') {               
                    steps {                    
                        sh "mvn compile"                   
                    }     
            } 
            stage('Unit test'){
                steps {
                sh "mvn test"
                    
                }
            }
            stage('MVN Package'){
            steps {
                sh "mvn package"
            }
            }
    }
}
