# Deploy Kubernetes bootstrap token

**Variables:**

  - `kube_bootstrap_token:` Kubernetes bootstrap token. Default `a90d81632f0d19718e2d24ab1d4df117`

**Notes:**

  - You should generate token by `head -c 16 /dev/urandom | od -An -t x | tr -d ' '` command
