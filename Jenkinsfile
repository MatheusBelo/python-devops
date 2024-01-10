pipeline {
    agent any
    tools {
    maven 'maven' //ou java
  } 
  stages {
      stage ('Instalar dependências') {
          steps {
          bat 'apt-get install python3.9 -y'
          sh 'apt-get update'
          sh 'python3 --version'
          sh 'apt-get install python-pip'
          sh 'pip --version'
          sh 'pip install pyinstaller' //instalar o pyinstaller pyinstaller –onefile Gabarito.py
          }
      }
      stage('Build') {
          steps {
          sh 'pyinstaller -onefile olamundo.py'  
          //sh 'javac -cp . olamundo.java' //compilar o python
        }
      } 
      stage('Executa o arquivo compilado') {
          steps{
          sh 'olamundo.exe' //executar o python
        }        
      }
 }
}
