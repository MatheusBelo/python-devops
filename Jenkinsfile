pipeline {
    agent any
    tools {
    python 'python' //ou java
  } 
  stages {
      stage ('Instalar dependências') {
          steps {
          sh 'sudo apt-get install python3.9 -y'
          sh 'sudo apt-get update'
          sh 'python3 --version'
          sh 'sudo apt-get install python-pip'
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
