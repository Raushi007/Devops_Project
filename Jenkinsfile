pipeline{
    agent {
        label 'Master'
    }
    stages{
        stage('checkout'){
            steps{
                checkout scm
        }
    }
        stage('build'){
            steps {
                sh "mvn clean install"
        }
    }
}
}
