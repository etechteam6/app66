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
                echo "this is a prototype"
            }
        }
        stage('3-s3'){
            steps{
                sh 'pwd'
                sh 'du -h'
            }
        }
        stage(''){
            parallel{
        		stage('p1'){
        			steps{
        				echo "first parallel-stage"
        			}
        		}
        		stage('p2'){
        			steps{
        				echo "second parallel-stage"
        			}
        		}
        	}
        }
    }
}