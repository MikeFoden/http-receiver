# HTTP Receiver

A very simple Docker container for seeing what gets sent to a HTTP server.

Based off @mdonker's server.py gist located at https://gist.github.com/mdonkers/63e115cc0c79b4f6b8b3a6b797e485c7

## Running instructions

1. Clone this repository to your machine.

2. Build the Docker image

```
docker build -t receiver .
```

3. Run the container

```
docker run -d -p 8000:8000 --name receiver --rm receiver
```

4. Send your traffic to `localhost:8000`

5. Look through your container logs to see the payload that was sent through.

```
docker logs receiver
```