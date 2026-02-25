---
apiVersion: storage.k8s.io/v1
kind: StorageClass
metadata:
  name: ebs-sc
provisioner: ebs.csi.aws.com
volumeBindingMode: WaitForFirstConsumer
reclaimPolicy: Retain
---
---

 kubectl patch secret argocd-secret -n argocd --type merge -p '{"stringData": {"webhook.github.secret": "YOUR_GITHUB_WEBHOOK_SECRET"}}'
---
