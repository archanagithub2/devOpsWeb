pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "3.8.6"
    }
    
    stages {
        stage('Cloning'){
            steps{
            git branch: 'test-1.1', credentialsId: '985d100d-7c11-4742-8507-4590903871ad', url: 'https://github.com/archanagithub2/devOpsWeb.git'
            }
        }
        
        
       
        stage('Deploy'){
            steps{
        deploy adapters: [tomcat9(credentialsId: 'Tomacat 9', path: '', url: 'http://172.16.1.129:8181/')], contextPath: null, war: '**/*.war'
        }
       }
    }
}
