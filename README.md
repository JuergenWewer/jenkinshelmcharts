# Jenkins Community Kubernetes Helm Charts

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

The code is provided as-is with no warranties.

## Usage

[Helm](https://helm.sh) must be installed to use the charts.
Please refer to Helm's [documentation](https://helm.sh/docs/) to get started.

Once Helm is set up properly, add the repo as follows:

```console
helm repo add jenkins https://charts.jenkins.io
```

You can then run `helm search repo jenkins` to see the charts.

<!-- Keep full URL links to repo files because this README syncs from main to gh-pages.  -->
Chart documentation is available in [jenkins directory](https://github.com/jenkinsci/helm-charts/blob/main/charts/jenkins/README.md).

## Contributing

<!-- Keep full URL links to repo files because this README syncs from main to gh-pages.  -->
We'd love to have you contribute! Please refer to our [contribution guidelines](https://github.com/jenkinsci/helm-charts/blob/main/CONTRIBUTING.md) for details.

## License

<!-- Keep full URL links to repo files because this README syncs from main to gh-pages.  -->
[Apache 2.0 License](https://github.com/jenkinsci/helm-charts/blob/main/LICENSE).

export KUBECONFIG=/Users/wewer/.kube/master/etc/kubernetes/admin.conf

helm install jenkins ./charts/jenkins -n kube-system
kubectl exec --namespace kube-system -it svc/jenkins -c jenkins -- /bin/cat /run/secrets/chart-admin-password && echo

admin
kjUCu8bXkxuiBljYD5NNq3

kubectl --namespace kube-system port-forward svc/jenkins 8080:8080

http://127.0.0.1:8080
