pipeline {
 agent any
 
 stages {
 
 stage(‘Provision infrastructure’) {
 
 steps {
 dir(‘F:\SV_PetClinic\Terraform\terraform_0.12.20_windows_amd64’)
 {
 bat '''terraform init
'''
 bat '''terraform plan -out=plan
'''
 // sh ‘terraform destroy -auto-approve’
 bat '''terraform apply plan
'''
 }
 
 
 }
 }
 
 
 
 }
}
