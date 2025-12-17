# Nginx Health Check (EC2 via SSM)

## 目的
EC2上のnginxが起動しているか、localhostでHTTP応答できるかを確認する。

## 対象
- InstanceId: i-09848f58fbd3b432c
- Region: ap-northeast-1

## 手順

### 1) SSMで確認コマンドを実行（CommandIdを取得）
```bash
aws ssm send-command \
  --profile portfolio --region ap-northeast-1 \
  --document-name "AWS-RunShellScript" \
  --targets "Key=InstanceIds,Values=i-09848f58fbd3b432c" \
  --comment "portfolio: check nginx" \
  --parameters commands='["sudo systemctl status nginx --no-pager","curl -sS http://localhost/ | head"]' \
  --query "Command.CommandId" --output text

