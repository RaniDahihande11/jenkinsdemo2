pipeline{
    agent any

    environment{
        PYTHON = 'C:\\Users\\adity\\AppData\\Local\\Programs\\Python\\Python312\\python.exe'
        // create variable for use path easy way
    }
   

   
    stages{
        stage('Checkout Data'){
            steps{
                checkout scm
            }
           

        }
         stage('Extract Data'){
            steps{
             bat "${env.PYTHON} extractdata.py"
        }
         }

    }
      
    post{
         always {
            echo 'Pipeline completed.'
        }
       success {
            echo 'Pipeline completed.'
        }
        failure {
            echo 'Pipeline failed.'
        }

    }

   
}