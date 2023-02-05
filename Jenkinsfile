pipeline{
    agent any

    environment {
        NAME = "Stage2"
    }

    stages{
            stage('code deploy'){
                steps{
                       ansiblePlaybook credentialsId: 'webserver', disableHostKeyChecking: true, installation: 'ansible', inventory: 'inventory.txt', playbook: 'Playbook.yaml'
                }
            }

           
    }

}
