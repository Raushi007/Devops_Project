  pipeline {
  agent any
  environment {
    AWS_DEFAULT_REGION="${params.REGION}"
  }
  stages {
    stage('AWS Instance Listing') {
      steps {
        sh '''
         aws ec2 describe-instances \
         --filters Name=tag-key,Values=Name \
         --query 'Reservations[*].Instances[*].{Instance:InstanceId,AZ:Placement.AvailabilityZone,PrivateIpAddress:PrivateIpAddress,Name:Tags[?Key==`Name`]|[0].Value}' \
         --output table
        '''
      }
    }
  }
}
