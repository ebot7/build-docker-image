# Build and Push Docker Images of core repos to ECR
A github action to build docker images for core repos and push them to ECR 

## Usage
Use the following as a step in your Github workflows.

```
- uses: ebot7/build-docker-image@master
  with:
    app-name: <app-name>
    ecr-repository: ebot7/<app-name>
    build-arg: 'FOO=123'
    dockerfile-path: <some-path> // defaults to ./Dockerfile
    aws-secret-access-key: {{ secrets.AWS_SECRET_ACCESS_KEY }}
    aws-access-key-id: {{ secrets.AWS_ACCESS_KEY_ID }}
```
Replace `<app-name>` with appropriate string before running