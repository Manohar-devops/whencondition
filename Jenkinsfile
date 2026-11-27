pipeline {
    agent any
    stages {
        stage ("Build Stage") {
            steps {
                echo "Building the application"
            }
        }
        stage ("Sonar Stage") {
            steps {
                echo "Scanning the application"
            }
        }
        stage ("Docker Image Stage") {
            steps {
                echo "Building the Docker Image"
            }
        }
        stage ("Docker Push Stage") {
            steps {
                echo "Pushing the docker image to docker registry"
            }
        }
        stage ("Dev Stage") {
            steps {
                echo "Deploying the application in Dev env"
            }
        }
        stage ("Test Stage") {
            steps {
                echo "Deploying the application in Test env"
            }
        } 
        stage ("Stage Stage") {
            when {
                branch "release/*"
            }
            steps {
                echo "Deploying the application to Stage env"
            }
        }
        stage ("Prod Stage") {
            when {
                // our application shoould deploy to prod only if app is going through tag
                //vx.x.x ==> v1.2.3
                tag pattern: "v\\d{1,2}\\.\\d{1,2}\\.\\d{1,2}", comparator: "REGEXP"
            }
            steps {
                echo "Building the application"
            }
        }       
    }
}
