# How to install Umbrella Chart


## From dev branch

## From RC/Offical release
1. Get the release tag from the repo for example https://github.com/h2oai/umbrella-chart/releases/tag/v2.0.0-rc4
2. `aws sso login --profile H2O-ECR-Access-353750902984`
3. `aws ecr get-login-password --region us-east-1 --profile H2O-ECR-Access-353750902984 | helm registry login --username AWS --password-stdin 353750902984.dkr.ecr.us-east-1.amazonaws.com`
4. `helm pull oci://353750902984.dkr.ecr.us-east-1.amazonaws.com/umbrella/h2oai-chart --version 2.0.0-rc4`
5. Create a k8 cluster if you havent
6. `az aks get-credentials --resource-group $RESOURCE_GROUP --name $CLUSTER_NAME --overwrite-existing`
