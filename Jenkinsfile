pipeline {
  agent {
    docker {
      image 'lilinj2000/dev:centos6.gcc'
    }
  }

  environment {
    home_3rd = '/var/jenkins_home/dist_pkg/3rd/centos6'
    home_libs = '/var/jenkins_home/dist_pkg/libs/centos6'
    home_app = '/var/jenkins_home/dist_pkg/app/centos6'
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
}
