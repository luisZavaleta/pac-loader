def imageName = 'luiszavaleta/pac-loader'

node{
    stage('Checkout'){
        checkout scm
    }
    stage('unit test'){
        sh "docker build -t ${imageName}-test -f Dockerfile.test ."
        sh "docker run --rm ${imageName}-test"
    }
}