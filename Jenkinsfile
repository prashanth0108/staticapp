node {
    stage('clone'){
        git'https://github.com/prashanth0108/index-file.git'
    }
    stage('image build'){
        sh'docker build -t project .'
    }
    stage('container'){
        sh'docker run --name prashanth -d -p 86:80 project'
    }
}