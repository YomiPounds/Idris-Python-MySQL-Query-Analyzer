pipeline {
    agent any
    stages{
        stage ("git checkout"){
            steps{
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'Abayomi-Git', url: 'https://github.com/YomiPounds/Idris-Python-MySQL-Query-Analyzer.git']])
            }
        }
        stage ("docker build image"){
            sh "docker build -t pounds-jenkins-image ."
        }
        stage ("docker login"){
            steps{
                sh "docker login -u yomipounds -p Devops2022"
            }
        }
    }
}