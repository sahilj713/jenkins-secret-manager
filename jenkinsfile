pipeline{
agent any
stages{
stage('get secret from secret manager'){
steps{
script{
sh '''#!/bin/bash
ENVFILE="env_file_brightree_api"
AWS_SECRET_ID="val/dev"
AWS_REGION="us-east-1"
​
echo "fetching envs from aws secrets manager"
​
# Export the secret to .env
for s in $(aws secretsmanager get-secret-value --secret-id $AWS_SECRET_ID --region $AWS_REGION |
    jq -r '.SecretString' |
    jq -r "to_entries|map(\"\(.key)=\(.value|tostring)\")|.[]"); do
    export $s
done
​
envsubst < env_template > $ENVFILE
​
echo "finished writing envs"
cat env_file_brightree_api
'''
}
}
}
}
}
