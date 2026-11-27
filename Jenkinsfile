pipeline {
    agent any
    parameters {
        string(name: 'Person', defaultValue: 'Manu', description: 'Enter your name')
    }
    stages {
        stage ("Parameter stage") {
            steps {
                echo "Wlcome to ${params.Person}"
            }
        }
    }
}
