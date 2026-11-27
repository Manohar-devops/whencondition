pipeline {
    agent any
    stages {
        stage ("Build Stage") {
            steps {
                echo "Building the application"
            }
        }
        stage ("When Stage") {
            when {
                expression {
                    BRANCH_NAME ==~ /(production|staging)/
                }
            }
            steps {
                echo "Deploying when Stage to Prod"
            }
        }
    }
}
