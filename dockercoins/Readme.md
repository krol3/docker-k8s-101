# Dockercoins

[Container trainning - dockercoins](https://github.com/jpetazzo/container.training/tree/master/dockercoins)

DockerCoins is made of 5 services:

- rng = web service generating random bytes

- hasher = web service computing hash of POSTed data

- worker = background process calling rng and hasher

- webui = web interface to watch progress

- redis = data store (holds a counter updated by worker)