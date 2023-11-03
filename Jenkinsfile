pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'Apache Maven 3.8.6') {
                    sh 'mvn clean package'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'Apache Maven 3.8.6') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'Apache Maven 3.8.6') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
