# Build and Push Docker Images of core repos to ECR
A github action to build docker images for core repos and push them to ECR 

## Usage
Use the following as a step in your Github workflows.

```
- uses: ebot7/build-docker-image@master
  with:
    app-name: <app-name>
    ecr-repository: ebot7/<app-name>
    aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }}
    aws-secret-access-key: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
```
Replace `<app-name>` with appropriate string before running

## Options

- `app-name`: The name of the application. This will be removed soon but is currently needed for backwards-compatibility.
- `ecr-repository`: the docker repository to which to push the image. Typically `ebot7/<app-name>`.
- `build-args`: Specify one or more build arguments passed to the Docker build. This should be in the format `ARG_NAME=value`. Empty by default. If several arguments are desired, pass them using 
```
|
  ARG_NAME=value
  ARG_NAME_2=value2
```
- `dockerfile-path`: The path to the Dockerfile relative to the repository root. Defaults to `./Dockerfile`.
- `aws-access-key-id`: The AWS access key ID used to access the Docker registry.
- `aws-secret-access-key`: The AWS secret access key used to access the Docker registry.
