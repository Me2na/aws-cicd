pipeline {
 agent any

stages{
  stage ('git checkout'){
steps{
    git branch: 'main', url: 'https://github.com/Me2na/aws-cicd.git'
 }
}
stage ('test'){
  steps{
    sh 'echo test'
  }
}
}
}