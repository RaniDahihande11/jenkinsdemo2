pipeline{
    agent any

    environment{
        PYTHON = 'C:\\Users\\adity\\AppData\\Local\\Programs\\Python\\Python312\\python.exe'
        // create variable for use path easy way
    }

    triggers{
        cron("*/2 * * * *") // for every 2 min
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



// Scripted/ groovy script

// node{
//     try{
//         stage('Checkout Code'){

//             checkout scm


//         }
//         stage('Extract Data'){
//             bat "C:\\Users\\adity\\AppData\\Local\\Programs\\Python\\Python312\\python.exe extractdata.py"

//         }
//     }
//     catch(err){
//         echo "Pipeline Error: ${err}"

//     }
//     finally{
//         echo 'Pipeline completed'
//     }
// }