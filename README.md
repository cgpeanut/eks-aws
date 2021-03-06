# eks-aws: Description
--- 
# Description:
  Launch an EKS cluster with three worker nodes in the us-east-1 region. Then, create a Deployment, and a Pod running container instances using the public nginx image. Then, expose your application to the internet by adding a LoadBalancer service.

- https://parveensingh.com/packer-golden-vm-image-with-azure-devops/


This repo will describe the use of AWS command line interface and console,
eksctl and kubectl to launch and EKS cluster, provision a Kubernetes deploymnet-
and pod running instances of nginx, create a LoadBalancer service to expose your
application over the internet.

# My Objective:
---
    step 1: Create an IAM User with Admin Rights:
    1.  Create sn IAM user with programmatic access and admintrator priveleges.
    2.  Take nore of the access key and secret acess key you'll need them.

    step 2: Launch an EC2 instance and configure the commanc line tools.
    1.  Create and EC2 instance in us-east-1 region.
    2.  Upgrade the AWS CLKI on your EC2 instance to CLI v2x or later. 
    3.  configure the AWS CLI using the credentials you created. 
    4.  Install elctl on EC2 instance
    5.  Install kubectl on EC2 instance

    step 3: Provision an EKS cluster
    1. Use eksctl to provision an EKS cluster with three worker nodes in us-east-1
    2. Use Kubernetes vrsion 1.16 or later.

    step 4: Create a Deployment on Your EKS Cluster
      1.  Download source code from your github repo: https://github.com/cgpeanut/eks-aws.git
      2.  Use kubectl to create a LoadBalancer service
      3.  Check the status of your cluster deployment, and pods unsing kubectl.
      4.  When the Deployment is up an running, check that you can access your application using DNS name of the LoadBalancer. 

    step 5: Test the High Availability Features of the Newly created EKS cluster. 
      1. In the AWS Console, shut down all the worker nodes.
      2. Check the status of your cluster, deployment and pods using kubectl.
      3. After a few minutes, you should see EKS launching new instances to keep you service running,
      4. When the cluster is back to a steady state, check that your application is up and running.

