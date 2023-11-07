# My first docker image

## Notes

* `Dockerfile` is the key
  
  * Provide *instructions* and *arguments* in the file.

  * Use `FROM` to pick a base image. Always choose official/org approved base image.
    
  * You can `COPY` local files into the image.
  
  * Images are golden copies, which are read only.

  * Containers are running instances of an image.

* To build image: `docker build -t nginx:1.0`, where `-t` tells the tag name.

* To test image: `docker run -d -p 9090:80 --name webserver nginx:1.0`, where:
  * `-d` means run in detached mode
  * `-p` maps port 80 inside the container to 9090 external
  * `--name` gives name of the container
  * Finally the image and tag must be provided