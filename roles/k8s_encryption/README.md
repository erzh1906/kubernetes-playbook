# Deploy Kubernetes encryption key for encryption Kubernetes Secrets

**Variables:**

  - `kube_encryption_key:` Kubernetes encryption key. Default `Aeb0eNp576qMFof+m2GsCW1Nti2gPeoJeNd5ca+2RYI=`

**Notes:**

  - You should generate token by `head -c 32 /dev/urandom | base64` command
