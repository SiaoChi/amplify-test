# AWS Amplify deploy

## Deploy frontend project
1. Connect to github repo
2. Finish deploy File which should be docker

Below is the sample dockerfile

```
version: 1
frontend:
  phases:
    # IMPORTANT - Please verify your build commands
    build:
      commands: []  ex. npm run build
  artifacts:
    # IMPORTANT - Please verify your build output directory
    baseDirectory: /
    files:
      - '**/*'
  cache:
    paths: []
```
<img width="1090" alt="截圖 2024-02-01 下午4 13 33" src="https://github.com/SiaoChi/amplify-test/assets/98171354/66ab697f-bf20-45a4-9cc0-793ac9a5d29a">
