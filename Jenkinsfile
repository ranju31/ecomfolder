pipeline{
  agent any
  tools{
    maven 'M3'
    jdk 'JAVA_HOME'
  }
  stages{
    stage('Checkout'){
      steps{
        git branch: 'master',url:'https://github.com/ranju31/ecomfolder.git'
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
      bat 'java -jar C:\Users\pdomedehalliogp\Desktop\spring boot\ECommerce-Angular-Spring-master\ecommercebackend/target/ecommercebackend-0.0.1-SNAPSHOT.jar'
    }
  }
}
}
