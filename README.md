# k8s-cloudflared

### Deploy cloudflared as a DaemonSet to send traffic to your cluster.

## Usage
The values for the tunnel and credentials.json in
the ConfigMap and SealedSecret resource are null. If the values are not being replaced, the pod will not start.
Therefore, I recommend copying the ConfigMap and SealedSecret resource,
insert your own values and patch them with kustomize. As a default service in the ConfigMap,
cloudflared sends all traffic to a nginx ingress controller (but you can replace this if you have a different setup).
