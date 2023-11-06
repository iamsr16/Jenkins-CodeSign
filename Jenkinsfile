pipeline {
    agent any 
      tools 
        {
          maven "Apache Maven 3.8.6"
        }

    stages{
        stage ('Building Stage') {

            steps {
                 sh 'mvn clean package'
                }
            }

        stage ('Code Signing') {
            steps {
                script {
                    sh 'Jarsigner -keystore None -storetype AzureKeyVault -signedjar signerjar.jar jenkins-example-1.0-SNAPSHOT.jar myalias -storepass "" -verbose'

               }
            }
         }
     }
}
