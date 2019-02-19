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
        sh 'sudo cp /var/lib/jenkins/workspace/sample-java/target/demo.war /var/lib/docker/tmp/docker-builder*'
        sh 'pwd'
        sh 'docker build -t naveenhm/demo-war .'
        sh 'docker run --rm -p 8081:8080 -d demo-java'
        
      }
    }
  }
}
