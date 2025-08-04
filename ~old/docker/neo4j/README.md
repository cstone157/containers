# Example Neo4j container


## For the helm chart - run (https://helm.sh/docs/chart_template_guide/getting_started/)
$ helm install full-coral ./helm

## View the manifest of our helm
$ helm get manifest full-coral

## Uninstall our release
$ helm uninstall full-coral

## Debugging install
$ helm install --debug --dry-run goodly-guppy ./helm

