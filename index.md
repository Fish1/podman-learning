# Build the images

`podman build -t localhost/learning/service1 .`
`podman build -t localhost/learning/service2 .`
`podman build -t localhost/learning/proxy .`

# Create the Pod

`podman run -dt --pod new:testpod -p 8080:80 localhost/learning/proxy`

# Add the containers to the Pod

`podman run -dt --pod testpod localhost/learning/service1`
`podman run -dt --pod testpod localhost/learning/service2`
