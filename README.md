# Build and Push Docker Images of core repos to ECR
A github action to build docker images for core repos and push them to ECR 

## Usage
Use the following as a step in your Github workflows.

```
- uses: ebot7/build-docker-image@master
  with:
    app-name: bot-engine
    ecr-repository: ebot7/bot-engine
    aws-secret-access-key: {{ secrets.AWS_SECRET_ACCESS_KEY }}
    aws-access-key-id: {{ secrets.AWS_ACCESS_KEY_ID }}
```
Replace bot-engine with appropriate string for other repos