# Pipeline to create and delete AWS EKS cluster using CircleCI

This is a simple pipeline using CircleCI. The idea is to be able to create a cluster in the cloud without having to install everything in a local machine


### Requirements

* CircleCI
* AWS EKS (Kubernetes)
* [**circleci/aws-eks@1.1.0s**](https://circleci.com/developer/orbs/orb/circleci/aws-eks)
* [**circleci/kubernetes@0.4.0**](https://circleci.com/developer/orbs/orb/circleci/kubernetes)

1. Create the CircleCI account

2. Create a GitHub repository

### Install

1. Download or clone this project

2. Push this project to your GitHub repository

3. In CircleCI setup the project.

Once on the Project page, find the project you are using and click Set Up Project.

![set up project](https://github.com/andresaaap/cicd-only-deploying-circleci/blob/main/img/set-up-project.png?raw=true)

According to the AWS EKS orb’s repo it is very important to meet these requirements before running the pipeline:

Add the AWS credentials as environment variables. Configure `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY` and `AWS_DEFAULT_REGION` as CircleCI project or context environment variables as shown in the links provided for [project](https://circleci.com/docs/2.0/env-vars/#setting-an-environment-variable-in-a-project) or [context](https://circleci.com/docs/2.0/env-vars/#setting-an-environment-variable-in-a-context).

![create environment variables](https://github.com/andresaaap/cicd-only-deploying-circleci/blob/main/img/create-env-variables.png?raw=true)

Add the policies to the IAM user suggested in the official eksctl website as [Minimum IAM policies](https://eksctl.io/usage/minimum-iam-policies/)

### Usage

Run the Pipeline by pushing a new commit to the GitHub repository or manually in the project’s GUI in CircleCI


### Links & Resources

* [**create-eks-cluster | CircleCI**](https://circleci.com/developer/orbs/orb/circleci/aws-eks#usage-create-eks-cluster)
