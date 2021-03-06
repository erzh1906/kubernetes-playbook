![Kubernetes Logo](https://raw.githubusercontent.com/kubernetes-sigs/kubespray/master/docs/img/kubernetes-logo.png)

# Deploy a Production Ready Kubernetes 1.13.0 - 1.16.7 Baremetal Cluster (Hardway like)

-   **Highly available** cluster
-   **ContainerD** runtime
-   **Weave** or **Flannel vxlan** CNI
-   **CentOS 7** only
-   **Nginx INC** ingress controller

#### Usage
  
    # Deploy your cluster
    ansible-playbook -i example.yml deploy_cluster.yml -e @extra_vars_example.yml

    # Scale up worker nodes
    ansible-playbook -i example.yml scaleup_workers.yml -e @extra_vars_example.yml

**Requirements:**
  - Ansible 2.9
  - You need servers with at least 4 CPUs for ETCD nodes

**Certificates variables:**

  - `kube_ca_crt_start_date:` CA certificates start date in ASN1 TIME format. Default `20190101000001Z`
  - `kube_ca_crt_expire_date:` CA certificates expire date in ASN1 TIME format. Default `20691231235959Z`

  - `kube_etcd_crt_start_date:` ETCD certificates start date in ASN1 TIME format. Default `20190101000001Z`
  - `kube_etcd_crt_expire_date:` ETCD certificates expire date in ASN1 TIME format. Default `20691231235959Z`

  - `kube_crt_start_date:` certificates start date in ASN1 TIME format. Default `20190101000001Z`
  - `kube_crt_expire_date:` certificates expire date in ASN1 TIME format. Default `20291231235959Z`

  - `kube_crt_country_name:` country name of certificate (C). Default `KZ`
  - `kube_crt_locality_name:` locality name of certificate (L). Default `Almaty`
  - `kube_crt_organizational_unit_name:` organization unit name of certificate (OU). Default `Kubernetes`
  - `kube_crt_organization_name:` organization name of certificate (O). Default `Aviata LLC`
  - `kube_crt_state_or_province_name:` state or province name of certificate (ST). Default `Almaty`

**Network variables:**

  - `kube_cni_type:` type of CNI. Can be `weave` or `flannel`. Default `weave`
  - `flannel_version:` version of Flannel CNI. Default `0.11.0`
  - `kube_pod_ip_range:` CIDR for pods network. Default `10.32.0.0/12`
  - `kube_service_cluster_ip_range:` network CIDR for Kubernetes services. Default `10.96.0.0/12`
  - `weave_version:` version of Weave CNI. Default `2.5.1`
  - `weave_password:` encryption password of Weave CNI. Default `06d3d0d67ca38a0925f7d2a7881d85ed5ff90173528f1daa7fa632ba832403ef5915cfbe2c87605c87209dc2eda1f2aa9e2fc9deb4a754904867eca1d5642b50cab144bbc1fc5be1d1868ccbe2ecac6c9aa13f9d8c4f6018e64c5156e95657c86c4fe4b365797bf9305caeb9a304c8b439ae7a3bd9730c4eaf64fd515cdd9b3c`

**DNS variables:**

  - `cluster_dns_type:` DNS server type for cluster. Can be `coredns` or `nodelocaldns`. Default `coredns`
  - `coredns_version:` version of CoreDNS. Default `1.5.0`
  - `coredns_replica_count:` desired count of CoreDNS instances. Default `4`
  - `nodelocaldns_version:` version of NodeLocalDNS. Default `1.15.5`
  - `coredns_service_ip:` IP address of CoreDNS Kubernetes service. Default `10.96.0.10`
  - `nodelocaldns_ip:` IP address of NodeLocalDNS cache. Default `169.254.25.10`

**Inventory related variables:**

  - `etcd_group_name:` inventory name of ETCD group. Default `etcd`
  - `masters_group_name:` inventory name of Kubernetes masters group. Default `masters`
  - `workers_group_name:` inventory name of Kubernetes workers group. Default `nodes`

**ETCD variables:**

  - `etcd_version:` version of ETCD. Default `3.4.0`

**Kubernetes variables:**

  - `kube_bootstrap_token:` Kubernetes bootstrap token. Default `a90d81632f0d19718e2d24ab1d4df117`
  - `kube_encryption_key:` Kubernetes encryption key. Default `"Aeb0eNp576qMFof+m2GsCW1Nti2gPeoJeNd5ca+2RYI="`
  - `kube_gid:` Linux group ID for pods runAsGroup securityContext. Default `2000`
  - `kube_uid:` Linux user ID for pods runAsUser securityContext. Default `2000`
  - `kube_version:` version of Kubernetes components. Default `1.13.12`
  - `metrics_server_version:` version of Metrics Server. Default `0.3.6`
  - `ingress_version:` version of Nginx INC. ingress controller. Default `1.4.6`

**Runtime variables:**

  - `containerd_repository:` repository of containerd package. `epel` and `docker-ce` available. Default `epel`
  - `containerd_ce_version:` version of containerd in Docker CE repository. Default `1.2.10-3.2`
  - `containerd_epel_version:` version of containerd in epel repository. Default `1.2.4-1`

**Notes:**

  - You should generate `kube_bootstrap_token` by `head -c 16 /dev/urandom | od -An -t x | tr -d ' '` command
  - You should generate `kube_encryption_key` by `head -c 32 /dev/urandom | base64` command
  - You should generate `weave_password` by `openssl rand -hex 128` command
  - Tested only on DigitalOcean droplets and AWS EC2
