def imageName = 'luiszavaleta/movies-loader'

node{
    stage('Checkout'){
        checkout scm
    }
    stage('unit test'){
        sh "sudo yum remove docker"
        sh "sudo amazon-linux-extras install docker"
        sh "sudo yum install docker"
        sh "sudo service docker start"
        sh "sudo usermod -a -G docker ec2-user"
        sh "docker info"
       
    }
}
