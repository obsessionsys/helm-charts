# Grafana-Beyla
The Helm chart for DaemonSet for ([Grafana Beyla](https://grafana.com/docs/beyla/latest/))

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

```
  helm repo add obsessionsys https://obsessionsys.github.io/helm-charts
```
If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo
obsessionsys` to see the charts.

To install the <chart-name> chart:

```
    helm install beyla obsessionsys/grafana-beyla
```
To uninstall the chart:

```
    helm delete beyla
```

For generated Helm Docs need to use command

```
docker run --rm --volume "$(pwd):/helm-docs" -u "$(id -u)" jnorwood/helm-docs:v1.8.1
```