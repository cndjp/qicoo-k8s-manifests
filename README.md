# qicoo-api-manifests-production
Production環境用のマニフェストを格納するリポジトリ

# secretの管理
以下で復号化します

```
gcloud kms decrypt \
    --location asia-northeast1 \
    --keyring qicoo-kms-02 \
    --key qicoo-kms-02-key   \
    --plaintext-file manifests/10_qicoo-api/11_config/13_qicoo-secret.yaml \
    --ciphertext-file manifests/10_qicoo-api/11_config/13_qicoo-secret.yaml.enc
```