pipeline {
    agent any
    options { buildDiscarder(logRotator(numToKeepStr: '10')) }
    triggers {
        cron('H 15 * * *')
    }
    stages {
        stage('Update') {
            steps {
                sh '/usr/local/bin/brew update'
            }
        }
        stage('Upgrade') {
            steps {
                sh '/usr/local/bin/brew upgrade'
            }
        }
    }
}
