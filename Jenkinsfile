pipeline {
    agent any
    tools {
        mvn 'maven'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('Static Code Analysis') {
            steps {
                // Execute FindBugs
                sh 'mvn findbugs:findbugs'

                // Execute PMD
                sh 'mvn pmd:pmd'
            }
        }
    }
}
