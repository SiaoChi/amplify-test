# AWS Amplify deploy

## Deploy frontend project
1. Connect to github repo
2. Finish deploy File which should be docker 

### amplify config file
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

### amplify config file , another sample
```
version: 1
backend:
  phases:
    build:
      commands:
        - '# Execute Amplify CLI with the helper script'
        - amplifyPush --simple
frontend:
  phases:
    preBuild:
      commands:
        - npm config set strict-ssl false
        - npm install --legacy-peer-deps
    build:
      commands:
        - npm run build
  artifacts:
    # IMPORTANT - Please verify your build output directory
    baseDirectory: build
    files:
      - '**/*'
  cache:
    paths:
      - node_modules/**/*

```

<img width="1090" alt="截圖 2024-02-01 下午4 13 33" src="https://github.com/SiaoChi/amplify-test/assets/98171354/66ab697f-bf20-45a4-9cc0-793ac9a5d29a">
