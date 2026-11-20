@Library('jenkins-shared-library') _

def configMap=[
    project="roboshop"
    component="catalogue"
    deploy_to ="dev"
]

echo "here we are deploying the catalogue"

if( env.BRANCH_NAME.equalsIgnoreCase("main") ){
    echo "please folow the RP"
}
else{
    jenkinsEKS(configMap)
}