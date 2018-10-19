# Running
Create a vault file:
``` ansible-vault create rhel_vault.yaml ```
Add in the following:
```
sm_username: <subscription manager username>
sm_password: <subscription manager password>
git_username: <git_username>
git_password: <git_password>
git_email: <git email address>
AWS_ACCESS_KEY_ID: "some key"
AWS_SECRET_ACCESS_KEY: "some key"
AWS_DEFAULT_REGION: "some key"
```


If you want to use git repos create a file named: repo_vars.yaml
Use the example repo_vars_example.yaml to specify the base host, then the repo names

Run:
```vagrant up```
