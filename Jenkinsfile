def imageName = 'luiszavaleta/movies-loader'

node{
    stage('Checkout'){
        checkout scm
    }

    
    stage('docker status '){
        sh "usermod -a -G docker jenkins"
        sh "docker run hello-world"
    }
    
  
}
