# Running
Create a vault file:
``` ansible-vault create rhel_vault.yaml```
Add in the following:
```
sm_username: <subscription manager username>
sm_password: <subscription manager password>
git_username: <git_username>
git_password: <git_password>
AWS_ACCESS_KEY_ID: "some key"
AWS_SECRET_ACCESS_KEY: "some key"
AWS_DEFAULT_REGION: "some key"
```

Run:
```vagrant up```
