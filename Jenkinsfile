  pipeline {
  agent any
  environment {
    AWS_DEFAULT_REGION="${params.REGION}"
  }
  stages {
    stage('AWS') {
      steps {
        sh '''
         aws ec2 describe-instances \
         --filters Name=tag-key,Values=Name \
         --query 'Reservations[*].Instances[*].{Instance:InstanceId,AZ:Placement.AvailabilityZone,PrivateIpAddress:PrivateIpAddress,Name:Tags[?Key==`Name`]|[0].Value}' \
         --output table >> output.txt
         aws s3 mv /var/lib/jenkins/workspace/pipeline/output.txt s3://my-nodejs-app-0
        '''
      }
    }
  }
}
