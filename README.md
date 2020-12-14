# dockerfiles

# how to build docker image from dockerfile and upload to remote repository?

http://blog.shippable.com/build-a-docker-image-and-push-it-to-docker-hub


# build docker image
e.g. sudo docker build -t shawndeu/cuda10.2-cudnn8:ros_melodic .
# push local docker image to repo
e.g. sudo docker push shawndeu/ros_melodic_full:cuda10.2-cudnn7

# run with nvidia
e.g. sudo docker run --gpus all -it shawndeu/xx:00