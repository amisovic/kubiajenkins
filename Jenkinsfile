pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }

    stages {
        stage('Build') {
            steps {
                sh "docker build -t amisovic/kubia:${BUILD_NUMBER} ."
                sh "sleep 300"

            }

            post {
                success {
                    println("Sve OK")
                }
            }
        }
    }
}


