# Unifi Network Controller

deploy Unifi Network Controller to on-premise k8s cluster 

## requirements

- ingress-nginx
- nfs-subdir-external-provisioner 

It needs to change `.Values.pvc.storageClassName`.
And make sure to allow these ports access

| Protocol | number | description |
| -- | -- | -- |
| TCP | 80 | web GUI | 
| TCP | 443 | web GUI | 
| TCP | 8080 | inform | 
| TCP | 8443 |  | 
| TCP | 8880 |  | 
| UDP | 3478 | STUN | 
| UDP | 10001 | find L2 device | 

## install

`helm install [RELEASE_NAME] im-neko/unifi-controller`
