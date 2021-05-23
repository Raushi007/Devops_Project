pipeline{
    agent any
    tools  {
       maven 'M2_HOME'
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
