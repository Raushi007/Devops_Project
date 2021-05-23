pipeline{
    {
        label 'master'
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
