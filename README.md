## :whale: docker-php

A collection of Docker images for PHP applications that I use in my personal projects.

### Pushing images to repository

1. Build your Docker image and tag it locally
```
docker build -t 8.3-swoole:latest .
```

2. Tag the image using your repository URL
```
docker tag 8.3-swoole:latest <repository>/8.3-swoole:latest
```

3. Push the Image to repository
```
docker push <repository>/8.3-swoole:latest
```
