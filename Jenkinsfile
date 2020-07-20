
pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                
                echo "checkout from SCM"
                
                git 'https://github.com/webweb04/python-scripts.git'
                // Make the output directory.
                
                echo "debug"
                sh "mkdir -p output"

                sh "ls -r"



                sh "pwd"


                // Write an useful file, which is needed to be archived.
                writeFile file: "output/usefulfile.txt", text: "This file is useful, need to archive it."

                // Write an useless file, which is not needed to be archived.
                writeFile file: "output/uselessfile.md", text: "This file is useless, no need to archive it."

                echo "Archive build output"

                // Archive the build output artifacts.
                archiveArtifacts artifacts: 'output/*.txt', excludes: 'output/*.md'
            }
        }
        stage('Test') { 
            steps {
                // 
            }
        }
        stage('Deploy') { 
            steps {
                // 
            }
        }
    }
}
