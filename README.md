# aws-ops-runbook-portfolio

## What this is
- OpenTofuでEC2 + SecurityGroup + SSM Roleを最小構成で作成
- SSM Run Commandでnginx稼働 & localhost HTTP 応答を確認するRunbookを用意

## Quick demo
- Deploy: `cd terraform && tofu init && tofu apply`
- Check nginx via SSM: `runbooks/nginx-healthcheck.md`
- Destroy: `cd terraform && tofu destroy`
