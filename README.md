# Encryption

This repository provides mutual TLS (mTLS) encryption between services on the platform.

## Usage 

For the first time setup, execute `bootstrap.sh`. Afterwards, you can use `skaffold dev`.

## Contributing 

### Updating 

You update Istio by executing `helm dependency update` in the `helm` directory.
