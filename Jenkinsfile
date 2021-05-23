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
                echo "M2_HOME = ${M2_HOME}"
                sh "mvn clean install"
        }
    }
}
}
