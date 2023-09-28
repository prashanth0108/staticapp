node {
    stage('checkout'){
        checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/prashanth0108/staticapp.git']])
    }
    stage ('build image'){
        sh'''docker build -t prashu1 .'''
    }
    stage('run container'){
        sh'''docker run --name web2 -d -p 88:80 prashu1:latest'''
    }
}
