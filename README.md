# openshift-fusion-access-manifests

This holds *testing* manifests only

```
* manifests/5.2.3.1.dev1 - v5.2.3.1_2025_05_12.18_17_21 DEV build
* manifests/5.2.3.1.dev2 - v5.2.3.1_2025_05_21.21_24_27 DEV build
* manifests/5.2.3.1.dev3 - v5.2.3.1_2025_06_11.11_08_52 DEV build
```

For example, to use the dev2 code drop, create the following FusionAccess CR:

```
apiVersion: fusion.storage.openshift.io/v1alpha1
kind: FusionAccess
metadata:
  name: fusionaccess-object
  namespace: ibm-fusion-access
spec:
  externalManifestURL: https://raw.githubusercontent.com/openshift-storage-scale/openshift-fusion-access-manifests/refs/heads/main/manifests/5.2.3.1.dev2/install.yaml
  storagedevicediscovery:
    create: true
```
