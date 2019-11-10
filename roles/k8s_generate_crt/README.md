# Generate certificates for Kubernetes and ETCD clusters

**Requirements:**
  - You need to have 4 groups in your inventory as defined in `etcd_group_name`, `masters_group_name`, `workers_group_name`, `loadbalancers_group_name` variables
  - You need to have common FQDN as defined in `kube_loadbalancer_fqdn` variable for all your loadbalancers IPs

**Variables:**

  - `kube_crt_country_name:` country name of certificate (C). Default `KZ`
  - `kube_crt_locality_name:` locality name of certificate (L). Default `Almaty`
  - `kube_crt_organization_name:` organization name of certificate (O). Default `Aviata LLC`
  - `kube_crt_organizational_unit_name:` organization unit name of certificate (OU). Default `Kubernetes`
  - `kube_crt_state_or_province_name:` state or province name of certificate (ST). Default `Almaty`
  - `kube_crt_start_date:` certificate start date in ASN1 TIME format. Default `20190101000001Z`
  - `kube_crt_expire_date:` certificate expire date in ASN1 TIME format. Default `20291231235959Z`
  - `kube_loadbalancer_fqdn:` loadbalancer FQDN name. Default `lb.cloud.example.com`
  - `kube_service_ip:` IP address of Kubernetes service. Default `172.30.0.1`
  - `etcd_group_name:` inventory name of ETCD group. Default `etcd`
  - `masters_group_name:` inventory name of Kubernetes masters group. Default `masters`
  - `workers_group_name:` inventory name of Kubernetes workers group. Default `nodes`
  - `loadbalancers_group_name:` inventory name of Kubernetes loadbalancers group. Default `loadbalancers`
