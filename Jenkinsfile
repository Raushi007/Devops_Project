pipeline{
    agent any
    
    stages{
        stage('checkout'){
            steps{
                checkout scm
        }
    }
        stage('build'){
            steps {
                sh "echo PATH = ${PATH}"
                
                sh "mvn clean install"
        }
    }
}
}
