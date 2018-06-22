pipeline {
  agent {
    docker {
      image 'lilinj2000/dev:centos7.gcc'
    }
  }

  environment {
    home_3rd = '/var/jenkins_home/dist_pkg/3rd/centos7'
    home_libs = '/var/jenkins_home/dist_pkg/libs/centos7'
    home_app = '/var/jenkins_home/dist_pkg/app/centos7'
  }

  stages {
    stage('install') {
      steps {
        sh '''
home_spdlog=${home_3rd}/spdlog
mkdir -p ${home_spdlog}
cp -avr include ${home_spdlog}
   	'''
      }
    }
  }
  post { 
    always { 
      cleanWs()
     }
  }
}
