# Encryption

This repository provides mutual TLS (mTLS) encryption between services on the platform.

## Usage 

For the first time setup, execute `bootstrap.sh`. Afterwards, you can use `skaffold dev`.

> [!IMPORTANT]
> Communication between encrypted services will stop working if encryption is up and you then shut it down. You fix this by simply putting encryption back up again.

You add encryption to a namespace or pod by labelling it with `psp/encrypt=true`.

## Contributing 

### Updating 

You update Istio by executing `helm dependency update` in the `helm` directory.
