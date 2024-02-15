# Helm Chart for Openshift using modified factoriotools image

## Usage Example

### Requirements
- helm cli
- logged into openshift cluster with oc cli, namespace admin rights
- Openshift Registry available
- only one release per namespace can have `createBuildResources: true` - those are shared per namespace

### Installation
- Clone this Repository
- Copy values.yaml to mypals.yaml
- Adjust values inside mypals.yaml to your needs
- Install Helm Chart
  > helm install mybelts . -f mybeltparadise.yaml
- If you changed values, just upgrade the helmchart
  > helm upgrade mybelts . -f mybeltparadise.yaml
