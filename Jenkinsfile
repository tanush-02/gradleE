pipeline {
    agent any

    tools {
        gradle 'Gradle'
        jdk 'JDK'
    }

    stages {
        stage('checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/tanush-02/gradleE.git'
            }
        }

        stage('build') {
            steps {
                sh 'gradle build'
            }
        }

        stage('test') {
            steps {
                sh 'gradle test'
            }
        }

        stage('Run application') {
            steps {
                sh 'gradle run'
            }
        }
    }

    post {
        success {
            echo 'Build Successful'
        }

        failure {
            echo 'Build Failed'
        }
    }
}
