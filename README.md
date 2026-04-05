# Encryption

This repository provides mutual TLS (mTLS) encryption between services on the platform.

## Usage 

For the first time setup, execute `bootstrap.sh`. Afterwards, you can use `skaffold dev`.

> [!IMPORTANT]
> Communication between encrypted services will stop working if encryption is up and you then shut it down. You fix this by simply putting encryption back up again.

All namespaces and pods use encryption by default.
For specific namespaces or pods, encryption can be disabled by labelling it with `psp.io/encryption=false`.

## Contributing 

### Updating 

You update Istio by executing `helm dependency update` in the `helm` directory.

### Verification

You can verify that traffic is being encrypted by using the following command, and looking for the desired traffic:
```
kubectl logs daemonsets/ztunnel -n istio-system
```
