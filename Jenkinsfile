pipeline {
 agent any

environment{
  BRANCH_NAME = 'main'
  GIT_URL = 'https://github.com/Me2na/aws-cicd.git'
  IMAGE_TAG = 'awscicd'
  IMAGE_VERSION = "${BUILD_NUMBER}"
  }


stages{
 stage ('git checkout'){
  steps{
    git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
 }
}
 stage ('docker buil'){
  steps{
    sh 'docker build -t "${IMAGE_TAG}:${IMAGE_VERSION}".'
    sh 'docker images'
  }
}
}
}
