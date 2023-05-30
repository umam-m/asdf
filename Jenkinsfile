pipeline {
    agent any
    
    stages {
      stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
        stage('Log Example') {
            steps {
                script {
                    // Log a simple message
                    echo "This is a log message."
                    
                    // Log a variable value
                    def variable = "Hello, Jenkins!"
                    echo "The value of the variable is: ${variable}"
                    
                    // Log a complex object
                    def person = [
                        name: 'John Doe',
                        age: 30,
                        email: 'john.doe@example.com'
                    ]
                    echo "Person details: ${person}"
                }
            }
        }
    }
}
