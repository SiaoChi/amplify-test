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
