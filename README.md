## :whale: docker-php

A collection of Docker images for PHP applications that I use in my personal projects.

### Pushing images to repository

1. Authenticate
* [Docker Hub](https://github.com/danieltrolezi/laravel-app/wiki/01.-Setting-Up-Docker-on-Ubuntu#credential-store-docker-login)
* [AWS ECR](https://github.com/danieltrolezi/laravel-app/wiki/11.-AWS-Cookbook#configure-aws-sso)
* [GCP Artifact Registry](https://github.com/danieltrolezi/laravel-app/wiki/12.-GCP-Cookbook#installing-cli-gcloud)

2. Build your Docker image and tag it locally
```
docker build -t 8.3-swoole:latest .
```

3. Tag the image using your repository URL
```
docker tag 8.3-swoole:latest <repository>/8.3-swoole:latest
```

4. Push the Image to repository
```
docker push <repository>/8.3-swoole:latest
```
