# openshift-jq

Get pods with jq query for name, node and status.
```
oc get po -o json | jq -r '[.items[] | {Pod:.metadata.name, Node:.spec.nodeName, Status:.status.phase}]'
```
