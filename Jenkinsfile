
pipeline {

  agent{
   label "master"
  }
  stages{
  	stage('Git-Checkout'){
  		steps{
        git 'https://github.com/srgovardhanrao/mvp.git'
  		}
  	}
   stage('install'){
  	    steps{
sh label: '', script: '''cd twebs
/usr/local/bin/mvn clean install'''
          archiveArtifacts 'twebs/target/twebs.war'
        }
}
stage('deploy'){
  	    steps{
sh label: '', script: '''cp -R ../twebs.war /Users/govardhanrao/Downloads/apache-tomcat-8.5.61/webapps'''

}
  	}

  }

}

