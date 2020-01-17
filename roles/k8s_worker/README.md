# Upload core components manifests to Kubernetes master nodes


**Variables:**

  - `kube_version:` version of Kubernetes components. Default `1.13.0`
  - `etcd_group_name:` inventory name of ETCD group. Default `etcd`
  - `cluster_dns_type:` DNS server type for cluster. Can be `coredns` or `nodelocaldns`. Default `coredns`
  - `coredns_service_ip:` IP address of CoreDNS service. Default `172.30.0.10`
  - `nodelocaldns_ip:` IP address of NodeLocalDNS cache. Default `169.254.25.10`  
