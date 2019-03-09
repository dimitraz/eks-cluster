# Provisioning the cluster

<img width="60%" src="../images/diagram.png">

## Create the VPC and subnets

- A new VPC called `fyp-vpc`
- 3 Public subnets (`10.0.0.0/24, 10.0.1.0/24, 10.0.2.0/24`)
- 3 Private subnets (`10.0.3.0/24, 10.0.4.0/24, 10.0.5.0/24`). Each private subnet is tagged with `kubernetes.io/role/internal-elb:1`
- A `fyp-control-plane` security group for the VPC, which is applied to the Kubernetes master node later

Reference: https://docs.aws.amazon.com/eks/latest/userguide/create-public-private-vpc.html

## Create the cluster

- An EKS IAM role. Permissions are added by default when the type of trusted entity is AWS Service > EKS. This role is called `EKSServiceRole`
- Create the cluster. For `subnetIds` both the private and public subnet ids should be passed in:

```sh
aws eks --region eu-west-1 create-cluster \
--name fyp \
--role-arn <EKSServiceRole-arn> \
--resources-vpc-config subnetIds=<subnet-ids>,securityGroupIds=<fyp-control-plane-security-group-id>
```

- Configure kubectl to connect to the EKS cluster:

```sh
aws eks --region eu-west-1 update-kubeconfig --name fyp
```
