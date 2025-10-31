pipeline{
    agent any
    environment{
        PYTHON = 'C:\\Users\\adity\\AppData\\Local\\Programs\\Python\\Python312\\python.exe'
        // create variable for use path easy way
    }
    stages{
        stage('Checkout Data'){
            checkout scm

        }
         stage('Extract Data'){
            bat "${env.PYTHON}  extractdata.py"
        }

    }
    post{
        success{
            echo "success.."

        }
        failure{
            echo "failure..."

        }
        always{
            acho 'always...'

        }
    }
}