$ helm repo add prefect https://prefecthq.github.io/prefect-helm
$ helm install prefect-server prefect/prefect-server

$ kubectl --namespace default port-forward svc/prefect-server 4200:4200