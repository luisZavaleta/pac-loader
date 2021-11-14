def imageName = 'luiszavaleta/movies-loader'

node{
    stage('Checkout'){
        checkout scm
    }

    
    stage('docker status '){
        sh "systemctl status docker"
       
    }
    
     stage('docker hello '){
        sh "sudo docker run hello-world"
       
    }
}
