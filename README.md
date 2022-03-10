# vscode-remote-containers-aws-cdk-template

VSCode Remote Containers で AWS CDK プロジェクト始めるときのテンプレート

## aws sso memo

```bash
aws-sso-util login --profile gacha.dev
aws-sso-util credential-process --profile gacha.dev > auth.json
export AWS_ACCESS_KEY_ID=$(jq -r .AccessKeyId auth.json)
export AWS_SECRET_ACCESS_KEY=$(jq -r .SecretAccessKey auth.json)
export AWS_SESSION_TOKEN=$(jq -r .SessionToken auth.json)
rm auth.json
```