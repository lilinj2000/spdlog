pipeline {
  agent any
  stages {
    stage('install') {
      steps {
        sh '''kernel=`uname -sr | sed --e=\'s/ /\\//\'`

home_3rd=$JENKINS_HOME/3rd/${kernel}

home_spdlog=${home_3rd}/spdlog

mkdir -p ${home_spdlog}

cp -avr include ${home_spdlog}


'''
      }
    }
  }
}