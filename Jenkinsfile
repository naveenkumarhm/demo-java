pipeline{
  tools{
    maven 'M2_HOME'
  }
  agent any
  stages {
    stage ('build'){
      steps{
        echo 'Building the java-code'
        sh 'mvn clean install'
        sh 'pwd'
        sh 'docker build -t naveenhm/demo-war .'
      }
    }
  }
}
