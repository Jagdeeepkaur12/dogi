pipeline{
    agent any
    environment {
    FIREBASE_DEPLOY_TOKEN = credentials('Firebase-Token')
    }

 stages{
       
        stage('Testing Environment'){
            steps{
            sh 'firebase deploy -P test-681de --token "$FIREBASE_DEPLOY_TOKEN"'
            
            }
        } 
        stage('Staging Environment'){
            steps{

          sh 'firebase deploy -P dogi-b7679 --token "$FIREBASE_DEPLOY_TOKEN"'

         

             echo  'Building'
            }
        } 
        stage('Production Environment'){
            steps{
            sh 'firebase deploy -P stage-1b7ee --token "$FIREBASE_DEPLOY_TOKEN"'
            echo 'Production'
            }
        } 
    }

}
