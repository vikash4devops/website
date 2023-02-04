pipeline{
    agent any

    environment {
        NAME = "Stage2"
    }

    stages{
            stage('code clone'){
                steps{
                    sh "echo hello"
                }
            }
            //===================

            stage('code build'){
                steps{
                    sh "echo ${NAME} "
                }
            }

            stage('code deploy'){
                steps{
                    sh "echo code deployed "
                }
