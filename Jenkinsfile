pipeline {
 agent any
 
 stages {
 stage(‘checkout’) {
 steps {
 git 'https://github.com/kumarinn/jira-jenkins-shared-lib.git'
 
 }
 }
 stage(‘Set Terraform path’) {
 steps {
 script {
 def tfHome = tool name: ‘Terraform’
 env.PATH = “${tfHome}:${env.PATH}”
 }
 sh ‘terraform — version’
 
 
 }
 }
 
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
