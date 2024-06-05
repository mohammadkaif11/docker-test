pipeline {
agent { label 'Dev-Agent node' }
stages{
stage('Checkout'){
steps{
git url: 'https://github.com/mohammadkaif11/docker-jenkins-testing', branch: 'master'
 }
}

stage('Build'){
steps{
sh 'sudo docker build . -t kaif021/my-node-app:latest'
 }
}

stage('Test image') {
steps {
echo 'testing…'
sh 'sudo docker inspect -type=image kaif021/my-node-app:latest '
 }
}

stage('Push'){
steps{
sh 'sudo docker push kaif021/my-node-app:latest'
 }
}

// stage('Deploy'){
// steps{
//     }
  }
}