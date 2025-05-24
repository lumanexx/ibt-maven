pipeline {
    agent any
        stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Hi') {
            steps {
                echo 'Hi Emma'
            }
        }
        stage('DevOps') {
            steps {
                echo 'you will make it in tech'
            }
        }
        stage('Geology') {
            steps {
                echo 'your cgpa is 2.69'
            }
        }
        stage('Git') {
            steps {
                checkout scmGit(branches: [[name: '*/$Branch_Name']], extensions: [], userRemoteConfigs: [[credentialsId: 'Github-credential', url: 'https://github.com/lumanex/ibt-maven.git']])
                sh 'ls -lrt'
                sh 'echo $Branch_Name  $CHOICES'
                sh 'ls -al'
                sh 'ls -al'
                
            }
        }
        stage('hook') {
            steps {
                echo 'webhook is now working'
                echo 'sky is back'
                sh 'ls -l'
                
            }
        }
        stage('condition') {
            when{
                expression{
                    env.$Branch_Name=='main'
                }
            }
            steps {
                echo 'webhook is now working'
                echo 'sky is back'
                sh 'ls -l'
                
            }
        }
    }
}
