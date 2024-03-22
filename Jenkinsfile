pipeline {
    agent any
    tools {
        maven 'maven'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        // stage('Static Code Analysis') {
        //     steps {
        //         // Execute FindBugs
        //         sh 'mvn findbugs:findbugs'

        //         // Execute PMD
        //         sh 'mvn pmd:pmd'
        //     }
        // }
    }
}
