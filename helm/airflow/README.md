$ helm repo add apache-airflow https://airflow.apache.org
$ helm repo update apache-airflow
$ kubectl create ns airflow
$ helm install airflow apache-airflow/airflow --namespace airflow --debug --timeout 10m01s

$ kubectl port-forward svc/airflow-api-server 8080:8080 --namespace airflow


### Building the docker file that includes my dags
$ docker build --pull --tag my-dags:0.0.1 .

