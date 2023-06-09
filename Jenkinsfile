pipeline {
    agent any
    
    stages {
        stage('Build1') {
            steps {
                // Clean and build Xcode project
                sh "xcodebuild clean build -scheme RELEASE -workspace asdf.xcodeproj -sdk iphoneos"
            }
        }
        stage('Archive') {
            steps {
                // Archive the Xcode project
                sh "xcodebuild archive -scheme RELEASE -workspace <YOUR_WORKSPACE>.xcworkspace -archivePath build/asdf.xcarchive"
            }
        }
        
        stage('Export IPA') {
            steps {
                // Export the IPA file
                sh "xcodebuild -exportArchive -archivePath build/asdf.xcarchive -exportPath build -exportOptionsPlist exportOptions.plist"
            }
        }
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
