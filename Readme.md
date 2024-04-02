# Helm Chart for Openshift using modified factoriotools image

## Usage Example

### Requirements
- helm cli
- nfs server for storage, currently only static pvs with a fixed directory structure are supported, directory must be created manually on the nfs server
- if not using openshift: set `ocp: false` and `createBuildResources: false`
- logged into openshift cluster with oc cli, namespace admin rights
- Openshift Registry available
- only one release per namespace can have `createBuildResources: true` - those are shared per namespace

### Installation
- Clone this Repository
- Copy values.yaml to mybeltparadise.yaml
- Adjust values inside mybeltparadise.yaml to your needs
- Install Helm Chart
  > helm install mybelts . -f mybeltparadise.yaml
- If you changed values, just upgrade the helmchart
  > helm upgrade mybelts . -f mybeltparadise.yaml
