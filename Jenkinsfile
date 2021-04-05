pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }

    stages {
        stage('Build') {
            steps {
                sh "sleep 300"
                sh "docker build -t amisovic/kubia:${BUILD_NUMBER} ."
                sh "sleep 300"

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

            post {
                success {
                    println("Sve OK")
                }
            }
        }
    }
}


