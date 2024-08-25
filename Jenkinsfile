pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git url: '<remote-repository-url>'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Deploy') {
            steps {
                // Example of deployment step, adjust as needed
                deployToServer()
            }
        }
    }
}

def deployToServer() {
    // Implement your deployment logic here
    // Example: Copy the JAR file to a remote server
    sh 'scp target/my-java-app-1.0-SNAPSHOT.jar user@server:/path/to/deploy/'
}
