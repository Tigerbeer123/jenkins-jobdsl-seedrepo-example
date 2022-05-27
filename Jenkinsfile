node {
       stage('Clone') { 
              echo "1.Clone Stage" 
              git url: "https://github.com/Tigerbeer123/terraform-hw-github-actions.git" 
              script { 
                     build_tag = sh(returnStdout: true, script: 'git rev-parse --short HEAD').trim() 
              } 
       }
       
      stage ('Terraform init') {
         sh 'terraform init'
      } 
      stage ('Terraform Plan') {
         sh 'terraform plan'
      }
      stage ('Terraform Apply') {
          sh "terraform apply -auto-approve "
      }
      stage ('Terraform Destroy') {
          sh "terraform destroy -auto-approve "
      }
}
