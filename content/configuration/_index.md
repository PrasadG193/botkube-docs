---
title: "Configuration"
date: 2019-01-08T17:58:08+05:30
draft: false
weight: 20
---

BotKube controller reads configurations from **config.yaml** file placed at **CONFIG_PATH**

## config.yaml syntax
The configuration file contains, 

- Resource list you want to watch
- The type of events you want to get notifications about
- Way to skip filter runs
- Slack access configuration

```
  ## Resources you want to watch
  resources:
    - name: NAME_OF_THE_RESOURCE   # Name of the resources e.g pods, deployments, ingresses, etc. (Resource name must be in plural form)
      namespaces:                  # List of namespaces, "all" will watch all the namespaces
        - all
      events:                      # List of lifecycle events you want to receive, e.g create, update, delete OR all
        - create
        - delete
    - name: secrets
      namespaces:
        - kube-system
      events:
        - create
        - delete

  # K8S error/warning events you want to receive for the configured resources
  events:
    types:
      - normal
      - warning

  # Check true if you want to receive recommendations
  # about the best practices for the created resource
  recommendations: true
  
  # Channels configuration
  communications:
    slack:
      channel: 'SLACK_CHANNEL'
      token: 'SLACK_API_TOKEN'

  # Setting to support multiple clusters
  settings:
    # Cluster name to differentiate incoming messages
    clustername: not-configured
    # Set true to enable kubectl commands execution by BotKube on the cluster
    allowkubectl: false
```
The default configuration can be found at:
https://github.com/infracloudio/botkube/blob/master/config.yaml


As of now, BotKube can watch following types of resources:

- pods
- nodes
- services
- namespaces
- replicationcontrollers
- persistentvolumes
- persistentvolumeclaims
- secrets
- configmaps
- deployments
- daemonsets
- replicasets
- ingresses
- jobs
- roles
- rolebindings
- clusterroles
- clusterrolebindings

### Updating the configuration at runtime

You can update the configuration and use `helm upgrade` to update configuration values for the BotKube. 

You can also change values directly in ConfigMap - which is not reccomended but is great for quick experimentation. You have to edit the configmap which will also restart the BotKube pod to update mounted configuration in the pod.

```bash
$ kubectl edit configmap botkube-configmap -n botkube
```
This command will open configmap specs in an editor. Do the required changes, save and exit. The BotKube pod will automatically restart to have these configuration in effect.
