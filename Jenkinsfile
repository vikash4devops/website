pipeline{
    agent any

    environment {
        NAME = "Stage2"
    }

    stages{
            stage('code deploy'){
                steps{
                       withCredentials([sshUserPrivateKey(credentialsId: 'webserver', keyFileVariable: 'MY-KEY')]) {
                             sh "ansible-playbook Playbook.yaml -i Inventory.txt"
                        } 

                   
                }
            }
            

            stage('code build'){
                steps{
                    sh "echo ${NAME} "
                }
            }

            stage('code deploy'){
                steps{
                    sh "echo code deployed "
                }
            }
    }

}
