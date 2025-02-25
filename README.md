# kubectl-superdebug

An extension of `kubectl debug` that not only attaches starts a debugging pod sharing a process namespace with a target container in a running pod, but additionally copies that target container's volume specification to that of the ephemeral container.

For more information, check out my blog post on this:

[Debugging Running Pods on Kubernetes](https://medium.com/datamindedbe/debugging-running-pods-on-kubernetes-2ba160c47ef5)

## Limitations

This script was created as a proof-of-concept and for personal use. It is not ready to be industrialised or, say, submitted to the [krew project](https://github.com/kubernetes-sigs/krew) as-is.

This script does not implement all `kubectl debug` functionality, but only extends the functionality where your debugging container shares a process namespace with a target container specified by `--target`.
