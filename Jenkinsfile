pipeline{
    agent any
    tools {
  terraform 'Terraform'
}
stages{
    stage('git checkout'){
        steps{
           git branch: 'main', credentialsId: 'GitHub', url: 'https://github.com/galamsiva2020/Terraform_Practice-files.git'
        }
    }
    stage('Terraform initalization'){
        steps{
            sh 'terraform init'
        }
    }
    stage('Terraform showing plan'){
         steps{
             sh 'terraform plan'
         }
    }
    stage('Provisioning Resources'){
         steps{
             sh 'terraform apply --auto-approve'
              //sh 'terraform destroy --auto-approve'
         }
    }
}
}
