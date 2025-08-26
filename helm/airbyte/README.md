    $ helm repo add airbyte https://airbytehq.github.io/helm-charts
    $ helm repo update
    $ helm install airbyte airbyte/airbyte

    $ helm delete airbyte

# Added a postgres database

    $ kubectl apply -f ../../kube/base/airflow/secret.yaml
    $ kubectl apply -f ../../kube/base/postgres/pvc.yaml
    $ kubectl apply -f ../../kube/base/postgres/service.yaml
    $ kubectl apply -f ../../kube/base/postgres/deployment.yaml

# Added pgadmin

    $ kubectl apply -f ../../kube/base/pgadmin/pvc.yaml
    $ kubectl apply -f ../../kube/base/pgadmin/service.yaml
    $ kubectl apply -f ../../kube/base/pgadmin/deployment.yaml


# Port forwarding
    $ kubectl -n default port-forward deployment/pgadmin-deployment 80:80
    $ kubectl -n default port-forward deployment/airbyte-webapp 8080:8080