# Build and Push Docker Images of core repos to ECR
A github action to build docker images for core repos and push them to ECR 

## Usage
Use the following as a step in your Github workflows.

```
- uses: ebot7/build-docker-image@master
  with:
    app-name: bot-engine
    ecr-repository: ebot7/bot-engine
```
Replace bot-engine with appropriate string for other repos