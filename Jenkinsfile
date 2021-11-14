def imageName = 'luiszavaleta/movies-loader'

node{
    stage('Checkout'){
        checkout scm
    }

    
    stage('docker status '){
        sh "sudo systemctl status  -y docker"
       
    }
    
     stage('docker hello '){
        sh "sudo docker run hello-world"
       
    }
}
