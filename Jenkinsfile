pipeline{
    agent any
    stages{
        stage("Clone repository")
        {
            steps
            {
                git branch:'main',url:'https://github.com/bushrasayyed/Jenkins.git'
            }
        }
        stage("Install dependencies")
        {
            steps{
                sh 'npm install'
            }
        }
        //If you want to test enable this 
        // stage("Testing")
        // {
        //     steps{
        //         sh 'npm test'
        //     }
        // }
        stage("Start the app")
        {
            input{
                message'Do you want to start?'
                ok "Click on OK"
                submitter 'Bushra'
            }
          steps{
           sh 'npm start'
          }
        }
    }
}
