pipeline{
  agent any
  tools{
    maven 'M3'
    jdk 'JAVA_HOME'
  }
  stages{
    stage('Checkout'){
      steps{
        git branch: 'master',url:'git repo'
      }
    }
    stage('Build'){
      steps{
        bat 'mvn compile'
      }
    }
    stage('Package'){
      steps{
        bat 'mvn package'
      }
    }
    
    stage('Deploy'){
    steps{
      bat 'java -jar C:/Program Files/Jenkins/workspace/ecommercebackend/target/ecommercebackend-0.0.1-SNAPSHOT.jar'
    }
  }
}
}
