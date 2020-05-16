#!groovy
// Check ub1 properties
properties([disableConcurrentBuilds()])

pipeline {
    agent { 
        label 'raspberry3_agent'
        }
    options {
        buildDiscarder(logRotator(numToKeepStr: '10', artifactNumToKeepStr: '10'))
        timestamps()
    }
    stages {
        stage("First step") {
            steps {
                sh 'ssh pi@rasp \'hostname\''
            }
        }
        stage("Second step") {
            steps {
                sh 'ssh pi@rasp \'uptime\''
            }
        }
    }
}

