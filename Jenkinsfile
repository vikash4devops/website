pipeline{
    agent any

    environment {
        NAME = "Stage2"
        s_path = 
    }

    stages{

            stage('src path print'){
                steps{
                    sh 'echo $WORKSPACE'
                }
            }

            stage('code deploy'){
                steps{
                       ansiblePlaybook credentialsId: 'webserver', disableHostKeyChecking: true,extras: '-e src_path=$WORKSPACE', installation: 'ansible', inventory: 'inventory.txt', playbook: 'Playbook.yaml'
                }
            }

           
    }

}
