pipeline {
      agent any

          stages {

          stage('Maven build') {
                  buildInfo = rtMaven.run pom: 'maven-example/pom.xml', goals: 'clean install'
              }


           stage ('Testing Stage') {

                       steps {
                           withMaven(maven : 'maven_3_0_4') {
                               sh 'mvn test'
                           }
                       }
                   }

           stage ('Deployment any Stage') {
                       steps {
                           withMaven(maven : 'maven_3_5_0') {
                               sh 'mvn deploy'
                           }
                       }
                   }

          }
}