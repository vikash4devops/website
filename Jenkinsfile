pipeline{
    agent any

    environment {
        NAME = "Stage2"
    }

    stages{
            stage('code deploy'){
                steps{
                       ansiblePlaybook credentialsId: 'webserver', disableHostKeyChecking: true,extras: '-e src_path=$WORKSPACE', installation: 'ansible', inventory: 'inventory.txt', playbook: 'Playbook.yaml'
                }
            }

           
    }

}
