# EKS Kubernetes Cluster with Terraform

This project provisions a production-grade Kubernetes cluster on AWS using EKS and Terraform. It also demonstrates how to deploy a sample application using `kubectl`.

## 📌 Features

- AWS EKS Cluster (control plane)
- VPC with public subnets
- EKS Managed Node Group (AL2-based)
- IAM Roles with `aws-auth` mapping
- `kubectl` configured with `aws eks update-kubeconfig`
- Sample app (Nginx) deployed using LoadBalancer

## ⚙️ Tools & Services

- AWS (EKS, EC2, IAM, VPC, S3, DynamoDB)
- Terraform
- kubectl (CLI for Kubernetes)
- GitHub for version control

## 🚀 How to Deploy

**Clone the repo:**

   ```bash
   git clone https://github.com/your-username/eks-cluster-terraform.git
   cd eks-cluster-terraform
terraform init
terraform apply
aws eks --region us-east-1 update-kubeconfig --name devops-eks-cluster
kubectl apply -f nginx-deployment.yaml
kubectl get svc
Open in browser:
http://<EXTERNAL-IP>
