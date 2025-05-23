pipeline {
    agent any
    parameters{
        string(name:'Branch_Name', defaultValue:'main', description:'enter the branch to checkout')
        choice(name: 'CHOICES', choices: ['one', 'two', 'three'], description: 'choose a number') 
    }

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
            }
        }
        
    }
}
