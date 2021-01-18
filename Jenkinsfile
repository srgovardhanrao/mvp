
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
        }
}
stage('deploy'){
  	    steps{
sh label: '', script: '''cp /Users/govardhanrao/mavenp/mvp/twebs/target/twebs.war /Users/govardhanrao/Downloads/apache-tomcat-8.5.61/webapps'''

}
  	}

  }

}

