def imageName = 'luiszavaleta/movies-loader'

node{
    stage('Checkout'){
        checkout scm
    }

    
    stage('docker status '){
        sh "sudo yum -y remove docker"
         sh "sudo amazon-linux-extras install docker -y"
         sh "sudo service docker start"
         sh "sudo usermod -a -G docker ec2-user"
         sh "docker run hello-world"
       
    }
    
  
}
