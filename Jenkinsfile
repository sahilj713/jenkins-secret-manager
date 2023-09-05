pipeline{
agent any
stages{
stage('get secret from secret manager'){
steps{
script{
  sh '''
  pwd
  ls -l
  pwd
  chmod +x main.sh
  pwd
  ls -l
  . ./main.sh
  '''
}
}
}
}
}
