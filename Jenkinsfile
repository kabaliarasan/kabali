pipeline {
      agent any

          stages {

          stage ('Build') {
                      steps {
                          sh 'mvn clean package'
                      }
                  }


           stage ('Testing Stage') {

                       steps {

                               sh 'mvn test'

                       }
                   }

           stage ('Deployment any Stage') {

                       steps {

                               sh 'mvn install'
                           }
                       }
                   }


}