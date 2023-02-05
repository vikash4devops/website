pipeline{
    agent any

    environment {
        NAME = "Stage2"
    }

    stages{
            stage('code deploy'){
                steps{
                       withCredentials([sshUserPrivateKey(credentialsId: 'webserver', keyFileVariable: 'MY-KEY')]) {
                             sh "ansible-playbook Playbook.yaml -i inventory.txt"
                        } 

                   
                }
            }

           
    }

}
