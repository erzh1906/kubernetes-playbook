# Generate CA certificates for Kubernetes, ETCD and Front-Proxy

**Variables:**

  - `kube_crt_country_name:` country name of certificate (C). Default `KZ`
  - `kube_crt_locality_name:` locality name of certificate (L). Default `Almaty`
  - `kube_crt_organization_name:` organization name of certificate (O). Default `Aviata LLC`
  - `kube_crt_organizational_unit_name:` organization unit name of certificate (OU). Default `Kubernetes`
  - `kube_crt_state_or_province_name:` state or province name of certificate (ST). Default `Almaty`
  - `kube_ca_crt_start_date:` certificate start date in ASN1 TIME format. Default `20190101000001Z`
  - `kube_ca_crt_expire_date:` certificate expire date in ASN1 TIME format. Default `20691231235959Z`
