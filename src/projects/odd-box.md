# ODD-BOX

The first Rust based project I made open source: a reverse proxy server also doubling as a basic webserver. 

I had the idea for this project when having to keep multiple processes running, each with custom hostnames, on my local dev-machine (cardano node, indexer, marlowe-gql etc.) and could not find a way to orchestrate this without tools such as docker-compose, which was not a viable option at the time since I needed to be able to easily attach to the processes for debugging.

It works by letting you create a simple configuration file (toml format) and list a bunch of binary files along with a hostname for each.. and it will keep the processes running and act as a reverse proxy for the sites.  Fairly similar to what docker-compose does, just without containers, so that I can re-compile stuff while the system runs 🤯

The project is available on github: [OlofBlomqvist/odd-box](https://github.com/OlofBlomqvist/odd-box).

