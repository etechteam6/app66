pipeline{
    agent any 
    stages{
        stage('1-s1'){
            steps{
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-creds', url: 'https://github.com/etechteam6/app66.git']])
            }
        }
        stage('2-s2'){
            steps{
                sh 'lscpu'
                sh 'logname'
            }
        }
        stage(3-s3){
            steps{
                sh 'df -h'
                sh 'touch file1'
            }
        }
    }
}