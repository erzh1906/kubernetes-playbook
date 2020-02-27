# Deploy Weave CNI plugin

**Variables:**

  - `kube_cni_type:` type of CNI. Can be `weave` or `flannel`. Default `weave`
  - `flannel_version:` version of Flannel CNI. Default `0.11.0`
  - `weave_version:` version of Weave CNI. Default `2.5.1`
  - `weave_password:` encryption password of Weave CNI. Default `06d3d0d67ca38a0925f7d2a7881d85ed5ff90173528f1daa7fa632ba832403ef5915cfbe2c87605c87209dc2eda1f2aa9e2fc9deb4a754904867eca1d5642b50cab144bbc1fc5be1d1868ccbe2ecac6c9aa13f9d8c4f6018e64c5156e95657c86c4fe4b365797bf9305caeb9a304c8b439ae7a3bd9730c4eaf64fd515cdd9b3c`
  - `kube_pod_ip_range:` CIDR for pods network. Default `10.32.0.0/12`

**Notes:**

  - You should generate weave password by `openssl rand -hex 128` command
