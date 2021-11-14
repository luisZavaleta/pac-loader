def imageName = 'luiszavaleta/movies-loader'

node{
    stage('Checkout'){
        checkout scm
    }
    stage('unit test'){
        sh "yum remove docker"
        sh "amazon-linux-extras install docker"
        sh "yum install docker"
        sh "service docker start"
        sh "usermod -a -G docker ec2-user"
        sh "docker info"
       
    }
}
