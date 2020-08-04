pipeline {
    agent any

    stages {
        stage ('Build') {
            steps {
                sh 'mvn compile'
            }
        }

        stage ('Test') {
            steps {
                sh 'mvn test'
                junit 'target/*.xml'
                }
        }

        
        
        stage ('package'){
            steps {
                echo "Building war file"
                sh 'mvn package'
            }
        }
        
        stage ('Deploy Prerequites'){
            steps {
                echo "Moving the files to target machine"
                sh 'scp -i <key_path> <build_file> <user@ip>:<Location where to move the build file>'
            }
        }

        stage ('Deploy'){
            steps {
                echo "Deploy"
                sh 'ssh -i <key_path> <user@ip>:<script to be triggered>'
            }
        }


    }
}
