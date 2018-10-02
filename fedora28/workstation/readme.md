# Deployment

Create a vault file: ansible-vault create fedora_vault.yaml Add in the following:

```
AWS_ACCESS_KEY_ID: <AWS_ACCESS_KEY_ID>
AWS_SECRET_ACCESS_KEY: <AWS_SECRET_ACCESS_KEY>
AWS_DEFAULT_REGION: <AWS_DEFAULT_REGION>
```


Create a share folder named fedora_share in the vagrant home directory

Create a shared folder in virtualbox named fedora_share

Run: vagrant up
