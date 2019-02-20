### Notes for VSC

* Build inside docker for apps:
  * command + shift + p -> config tasks -> build c++ application -> "command": "./docker/docker.sh --build" 
  * docker/docker.sh: docker exec -it $(cat .$DEV_CONTAINER_NAME) make -j 4
  * command + shift + b
  
