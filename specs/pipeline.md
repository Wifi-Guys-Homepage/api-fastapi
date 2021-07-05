## Pipeline Requirements

### Dev - CI/CD
+ Test - pytest tox
+ Test - pytest tox e2e (future)
+ Build - buildah
+ Push - ECR
+ Deploy - terraform
+ PD Tests - call appinfo

### Prod - CD
+ Deploy - terraform
+ PD Tests - call appinfo
