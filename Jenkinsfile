pipeline{
    agent any
    tools {
        maven 'Maven 3.8.1
        
    }
    stages{
        stage('checkout'){
            steps{
                checkout scm
        }
    }
        stage('build'){
            steps {
                sh "echo PATH = ${PATH}"
                echo "M2_HOME = ${M2_HOME}"
                sh "mvn clean install"
        }
    }
}
}
