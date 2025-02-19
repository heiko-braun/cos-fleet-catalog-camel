# cos-fleet-catalog-camel

## Generating connectors catalog

* Connectors definition files are now generated automatically [after a merge to main](https://github.com/bf2fc6cc711aee1a0c2a/cos-fleet-catalog-camel/blob/main/.github/workflows/build-main.yaml).
* A PR will be created automatically in the [cos-manifests repo](https://github.com/bf2fc6cc711aee1a0c2a/cos-manifests/tree/main/connectors/cos-fleet-catalog-camel).
* The new generation system will only bump the revision of the impacted connectors.


## Generate resources locally

To generate the catalog sources locally for testing or validating changes:

1. Clone [cos-manifests](https://github.com/bf2fc6cc711aee1a0c2a/cos-manifests/)
1. Run the command bellow (update the path):
``` bash
./mvnw clean install -U -Dcos.connector.catalog.root=<path-to-local-cos-manifests/tree/main/connectors/cos-fleet-catalog-camel> -Dlog.enabled=true
```
1. Do a `git diff` in cos-manifests to see the changes.


