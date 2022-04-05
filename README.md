# RaiseTech AWSコース 第10回講義 課題

CloudFormationを利用したAWS環境の構築  
下記の構成図をCloudFormationを利用して構築する  
<img width="712" alt="AWS_RaiseTech" src="https://user-images.githubusercontent.com/50142017/161788383-5e7464ce-871e-486e-b606-dde53b75ba08.png">  
Cloud9で以下のコマンドを実行
### VPC
```
aws cloudformation create-stack --stack-name RaiseTech-cfn --template-body file://rt_vpc.yml
```
### Security Group
```
aws cloudformation create-stack --stack-name RaiseTech-cfn-sg --template-body file://rt_sg.yml
```
### IAM
```
aws cloudformation create-stack --stack-name RaiseTech-cfn-iam --template-body file://rt_iam.yml --capabilities CAPABILITY_NAMED_IAM
```
### EC2
```
aws cloudformation create-stack --stack-name RaiseTech-cfn-ec2 --template-body file://rt_ec2.yml --capabilities CAPABILITY_NAMED_IAM
```
### RDS(MySQL)
```
aws cloudformation create-stack --stack-name RaiseTech-cfn-rds --template-body file://rt_rds.yml
```
### ELB
```
aws cloudformation create-stack --stack-name RaiseTech-cfn-elb --template-body file://rt_elb.yml
```
### S3
```
aws cloudformation create-stack --stack-name RaiseTech-cfn-s3 --template-body file://rt_s3.yml
```
