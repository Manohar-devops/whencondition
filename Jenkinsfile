pipeline {
    agent any
    environment {
        Deploy_To = "Prod"
    }
    stages {
        stage ("When Stage") {
                when {
                    environment name: "Deploy_To", value: "Prod"
                }
                steps {
                    echo "Deploy to When Stage"
                }
        }
    }
}
