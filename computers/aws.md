<!-- TITLE: AWS -->
<!-- SUBTITLE: A quick summary of Aws -->

# Using 2FA aws-cli
```
aws sts get-session-token --serial-number arn-of-the-mfa-device --token-code code-from-token

set AWS_ACCESS_KEY_ID=<Access-Key-as-in-Previous-Output>
set AWS_SECRET_ACCESS_KEY=<Secret-Access-Key-as-in-Previous-Output>
set AWS_SESSION_TOKEN=<Session-Token-as-in-Previous-Output>
```