# Relative path

- [ ] aws configure --profile raynor
- [ ] aws iam list-attached-user-policies --user-name raynor --profile Raynor
- [ ] aws iam set-default-policy-version --policy-arn

Steps: 3
Completed: 0

# Absolute path

- [ ] aws configure --profile raynor
- [ ] aws iam list-attached-user-policies --user-name raynor --profile Raynor
- [ ] aws iam list-policy-versions --policy-arn <generatedARN>/cg-raynor-policy --profile Raynor
- [ ] aws iam get-policy-version --policy-arn <generatedARN>/cg-raynor-policy --version-id <versionID> --profile Raynor
- [ ] aws iam set-default-policy-version --policy-arn <generatedARN>/cg-raynor-policy --version-id <versionID> --profile Raynor

Steps: 5
Completed: 0
