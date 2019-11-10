# Upload core components manifests to Kubernetes master nodes


**Variables:**

  - `kube_version:` version of Kubernetes components. Default `1.13.0`
  - `etcd_group_name:` inventory name of ETCD group. Default `etcd`
  - `kube_service_cluster_ip_range:` network CIDR for Kubernetes services. Default `172.30.0.0/24`
  - `coredns_service_ip:` IP address of CoreDNS service. Default `172.30.0.10`
