.PHONY: build run start stop copy shell

IMAGE_NAME=softy-pinko:task1
CONTAINER_NAME=softy-pinko-task1

# Build the docker image
build:
	docker build -t $(IMAGE_NAME) .

# Run the docker container
run:
	docker run -p 5252:5252 -it --rm --name $(CONTAINER_NAME) $(IMAGE_NAME)

# Start the docker container
start:
	docker start $(CONTAINER_NAME)

# Stop the docker container
stop:
	docker stop $(CONTAINER_NAME)

# Copy files to the running container
copy:
	docker cp . $(CONTAINER_NAME):/app

# Open a shell inside the running container
shell:
	docker exec -it $(CONTAINER_NAME) /bin/bash
