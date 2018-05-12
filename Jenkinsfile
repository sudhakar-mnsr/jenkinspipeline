pipeline {
   agent { label 'sdl04302_agent' }
   tools {
      maven 'maven-3.5'
   }
   stages {
      stage ('checkout') {
         steps {
          git "https://github.com/sudhakar-mnsr/jenkinspipeline.git"
         }
      }
      stage ('compile') {
         steps {
            sh 'mvn clean compile'
         }
      }
      stage ('test') {
         steps {
            sh 'mvn test'
         }
      }
      stage ('package') {
         steps {
            sh 'mvn package'
         }
      }
   }
}
