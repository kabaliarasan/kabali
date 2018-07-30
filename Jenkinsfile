pipeline {
      agent any

          stages {
                stage ('Compile maven') {
                   steps {
                                   withMaven(maven : 'maven_3_0_4') {
                                       sh 'mvn clean compile'
                                   }
                               }
                }


           stage ('Testing Stage') {

                       steps {
                           withMaven(maven : 'maven_3_0_4') {
                               sh 'mvn test'
                           }
                       }
                   }

           stage ('Deployment Stage') {
                       steps {
                           withMaven(maven : 'maven_3_5_0') {
                               sh 'mvn deploy'
                           }
                       }
                   }

          }
}