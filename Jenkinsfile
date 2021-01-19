
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
    stage('test'){
  	    steps{
sh label: '', script: '''whoami'''

}
    }
stage('deploy'){
  	    steps{
sh label: '', script: '''curl -v -u admin:admin -T /Users/Shared/Jenkins/Home/workspace/simple t project/twebs/target/twebs.war 'http://localhost:8010//manager/text/deploy?path=rop''''

}
  	}

  }

}


