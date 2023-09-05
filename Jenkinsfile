pipeline{
agent any
stages{
stage('get secret from secret manager'){
steps{
  sh 'chmod +x main.sh'
  sh 'main.sh'
}
}
}
}
