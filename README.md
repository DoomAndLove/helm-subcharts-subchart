# helm-subcharts-subchart
A Helm Chart depending on a sub chart via file path which depends on sub charts via file path 

Testing a Bug in Argo where is does not find the subcharts subchart

## Helm Template top-chart output expected



```
---
# Source: top-chart/charts/middle-chart/charts/bottom-chart/templates/serviceaccount.yaml
apiVersion: v1
kind: ServiceAccount
metadata:
  name: release-name-bottom-chart
  labels:
    helm.sh/chart: bottom-chart-0.1.0
    app.kubernetes.io/name: bottom-chart
    app.kubernetes.io/instance: release-name
    app.kubernetes.io/version: "1.16.0"
    app.kubernetes.io/managed-by: Helm
---
# Source: top-chart/charts/middle-chart/templates/serviceaccount.yaml
apiVersion: v1
kind: ServiceAccount
metadata:
  name: release-name-middle-chart
  labels:
    helm.sh/chart: middle-chart-0.1.0
    app.kubernetes.io/name: middle-chart
    app.kubernetes.io/instance: release-name
    app.kubernetes.io/version: "1.16.0"
    app.kubernetes.io/managed-by: Helm
```
