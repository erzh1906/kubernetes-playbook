# Upload core components manifests to Kubernetes master nodes


**Variables:**

  - `kube_gid:` Linux group ID for pods runAsGroup securityContext. Default `2000`
  - `kube_uid:` Linux user ID for pods runAsUser securityContext. Default `2000`
  - `kube_crt_country_name:` country name of certificate (C). Default `KZ`
  - `kube_crt_locality_name:` locality name of certificate (L). Default `Almaty`
  - `kube_crt_organization_name:` organization name of certificate (O). Default `Aviata LLC`
  - `kube_crt_organizational_unit_name:` organization unit name of certificate (OU). Default `Kubernetes`
  - `kube_crt_state_or_province_name:` state or province name of certificate (ST). Default `Almaty`
  - `kube_crt_start_date:` certificate start date in ASN1 TIME format. Default `20190101000001Z`
  - `kube_crt_expire_date:` certificate expire date in ASN1 TIME format. Default `20291231235959Z`
  - `masters_group_name:` inventory name of Kubernetes masters group. Default `masters`
  - `kube_bootstrap_token:` Kubernetes bootstrap token. Default `a90d81632f0d19718e2d24ab1d4df117`
  - `kube_version:` version of Kubernetes components. Default `1.13.12`
  - `cluster_dns_type:` DNS server type for cluster. Can be `coredns` or `nodelocaldns`. Default `coredns`
  - `coredns_service_ip:` IP address of CoreDNS service. Default `10.96.0.10`
  - `nodelocaldns_ip:` IP address of NodeLocalDNS cache. Default `169.254.25.10`  

**Notes:**

  - You should generate token by `head -c 16 /dev/urandom | od -An -t x | tr -d ' '` command
