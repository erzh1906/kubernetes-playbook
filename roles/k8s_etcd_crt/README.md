# Generate ETCD certificates - server, peer, healthcheck-client and apiserver-etcd-client

**Requirements:**
  - You need to have ETCD group in your inventory as defined in `etcd_group_name` variable

**Variables:**

  - `kube_crt_country_name:` country name of certificate (C). Default `KZ`
  - `kube_crt_locality_name:` locality name of certificate (L). Default `Almaty`
  - `kube_crt_organization_name:` organization name of certificate (O). Default `Aviata LLC`
  - `kube_crt_organizational_unit_name:` organization unit name of certificate (OU). Default `Kubernetes`
  - `kube_crt_state_or_province_name:` state or province name of certificate (ST). Default `Almaty`
  - `kube_etcd_crt_start_date:` certificate start date in ASN1 TIME format. Default `20190101000001Z`
  - `kube_etcd_crt_expire_date:` certificate expire date in ASN1 TIME format. Default `20691231235959Z`
  - `etcd_group_name:` inventory name of ETCD group. Default `etcd`
