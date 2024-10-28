# GELF-LB

A simple to use UDP round-robin load-balancer for GELF packets (graylog messages) written in Rust.

Normally one would not be able to properly do round-robin loadblancing for GELF over UDP properly while using chunked packets as different chunks would end up on different servers, causing the messages to be discarded. 

This custom implementation will inspect each packet before forwarding, ensuring that all chunks for a specific message id go to the same backend.

The project can be found on github [here](https://github.com/OlofBlomqvist/gelf-lb).