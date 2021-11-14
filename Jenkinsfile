def imageName = 'luiszavaleta/movies-loader'

node{
    stage('Checkout'){
        checkout scm
    }
    stage('docker help'){
        sh "docker run --help"
        
       
    }
    
    stage('docker status '){
        sh "sudo systemctl status docker"
       
    }
    
     stage('docker hello '){
        sh "sudo docker run hello-world"
       
    }
}
