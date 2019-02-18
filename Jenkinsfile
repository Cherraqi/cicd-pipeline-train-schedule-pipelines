pipeline {
  agent any
  stages{
  stage('Build'){
  steps{
  echo 'Running build automation'
  sh './gradlew  build --no-daemon'
  archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
    stage('run'){
      steps{
      sh './gradlew build'
      sh   './gradlew npm_start &'
      }
    
    }
  }
}
