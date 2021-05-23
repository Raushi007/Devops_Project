pipeline{
    agent any
    enviromentt  {
        /opt/apache-maven-3.8.1/bin
    }
    
    stages{
        stage('checkout'){
            steps{
                checkout scm
        }
    }
        stage('build'){
            steps {
                echo "PATH = ${PATH}"
                
                sh "mvn clean install"
        }
    }
}
}
