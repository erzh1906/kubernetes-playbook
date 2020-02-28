# Install Kubernetes main packages and python modules for Ansible


**Variables:**

  - `kube_gid:` Linux group ID for pods runAsGroup securityContext. Default `2000`
  - `kube_uid:` Linux user ID for pods runAsUser securityContext. Default `2000`
  - `kube_version:` version of Kubernetes components. Default `1.13.12`
