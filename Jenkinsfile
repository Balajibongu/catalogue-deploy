@Library('jenkins-shared-library') _

def configMap = [
    project: "roboshop",
    component: "catalogue",
    deploy_to : "dev"
]

echo "here we are deploying the catalogue"
jenkinsEKS(configMap)