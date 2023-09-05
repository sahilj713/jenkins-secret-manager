pipeline{
agent any
stages{
stage('get secret from secret manager'){
steps{
script{
  sh '''
  chmod +x main.sh
  . ./main.sh
  '''
}
}
}
}
