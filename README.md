# WeCan on OpenShift

Openshift Template for WeCan backed by MongoDB

#### Create Template
```sh
oc create -f wecan.yml
```

#### Delete Instance Resources
Clean up all resources created. Note label filters assume single instance of template deployed in the current namespace.

```sh
oc delete all -l app=wecan
oc delete pods -l app=wecan
oc delete persistentvolumeclaim -l app=wecan
oc delete serviceaccount -l app=wecan
oc delete secret -l app=wecan
```
