# Hack / Dev single-node build

**Note: All scripts are assumed to be ran from this directory.**

## Generate assets

```
./bootkube-render
```

This will render all tls assets, manifests, secrets, and user-data files necessary to stand up a local vagrant based development cluster. If you would like to change configuration for any reason, you can tweak parameters found in the `config-env` file.

## Start VM

```
vagrant up
```
## Start Bootkube

```
./bootkube-up
```

Once all components are running, bootkube will shut itself down. After that, you will have a fully functional single-node self-hosted cluster with cluster DNS.

## Cleaning up

To stop the running cluster, run:

```
vagrant destroy -f
```