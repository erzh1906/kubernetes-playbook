# Upload core components manifests to Kubernetes master nodes


**Variables:**

  - `kube_version:` version of Kubernetes components. Default `1.13.0`
  - `kube_cni_type:` type of CNI. Can be `weave` or `flannel`. Default `weave`
  - `kube_pod_ip_range:` CIDR for pods network. Default `10.32.0.0/12`
  - `etcd_group_name:` inventory name of ETCD group. Default `etcd`
  - `kube_service_cluster_ip_range:` network CIDR for Kubernetes services. Default `172.30.0.0/24`
  - `cluster_dns_type:` DNS server type for cluster. Can be `coredns` or `nodelocaldns`. Default `coredns`
  - `coredns_service_ip:` IP address of CoreDNS service. Default `172.30.0.10`
  - `nodelocaldns_ip:` IP address of NodeLocalDNS cache. Default `169.254.25.10`
