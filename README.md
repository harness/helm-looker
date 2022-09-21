#Helm chart for looker

### Configuration options
For Chart configuration see the [README.md](src/looker/README.md) from the Chart.

### Publishing the Chart
Publishing of the Chart is done automatically by a Github workflow when a change is pushed to the `main` branch. Before merging to main please remember to manually update the version.

Bump version of the Chart in `src/looker/Chart.yaml`
```shell
OLD_VERSION=$(grep -E '^version:' src/looker/Chart.yaml | cut -d ' ' -f 2)
NEXT_VERSION=$(echo "$OLD_VERSION" | awk -F. '{print $1"."$2"."$3+1}')
sed -i -E -e "s/^version: ${OLD_VERSION}/version: ${NEXT_VERSION}/" src/looker/Chart.yaml
```
