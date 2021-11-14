def imageName = 'luiszavaleta/movies-loader'

node{
    stage('Checkout'){
        checkout scm
    }

    
    stage('docker status '){
        sh "sudo usermod -aG docker \$(whoami) -y"
         sh "docker run hello-world"
       
    }
    
  
}
