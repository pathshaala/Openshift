# Authentication and Authorization

# LAB: Add Cluster admin and dev group and user using htpasswd and remove kubeadmin.

## Configuring HTPASSWD Identity Provider
- ### create htpasswd authentication file. eg. htpasswd ~/ocp-auth/htpasswd
``` bash
$ touch ~/ocp-auth/htpasswd
```
- ### add user using htpasswd cmd.
  - **-c:** Stand for create new
  - **-B:** Stand for bcrypt encryption
  - **-b:** Password from the command line
  - **-D:** To delete user
``` bash
$ htpasswd -c -B -b ocp-auth/htpasswd \
admin password
```
- ### add another user
``` bash
$ htpasswd -b ocp-auth/htpasswd \
dev password

$ cat ocp-auth/htpasswd
admin:$2y$05$QPuzHdl06IDkJssT.tdkZuSmgjUHV1XeYU4FjxhQrFqKL7hs2ZKg8
dev:$apr1$0Nzmc1rh$yGtne1k.JX6L5s5wNa2zd.
```

- ### Secret for htpasswd user file
``` bash
$ oc login ...
$ oc create secret generic localuser \
--from-file htpasswd=/home/admin/ocp-auth/htpaswd \
-n openshift-config
```
- ### Assign the admin user the cluster-admin role
``` bash
$ oc adm policy add-cluster-role-to-user \
cluster-admin admin
```