pipeline{
    agent any
    enviromentt  {
       PATH = "/opt/apache-maven-3.8.1/bin:$PATH"
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
