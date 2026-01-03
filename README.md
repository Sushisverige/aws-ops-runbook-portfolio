# aws-ops-runbook-portfolio

## What this is
- OpenTofuでEC2 + SecurityGroup + SSM Roleを最小構成で作成
- SSM Run Commandでnginx稼働 & localhost HTTP 応答を確認するRunbookを用意

## Quick demo
- Deploy: `cd terraform && tofu init && tofu apply`
- Check nginx via SSM: `runbooks/nginx-healthcheck.md`
- Destroy: `cd terraform && tofu destroy`

## Safety
- `.terraform/` や `terraform.tfstate` はリポジトリに含めません（ローカル専用）
- 検証後は `tofu destroy` で必ず削除します

## Compliance / Privacy / Ethics
- This repository is provided as a sample/portfolio.
- Do not process personal/confidential data without proper authorization and consent.
- Review docs/DATA_HANDLING.md and docs/ETHICS.md before any real-world use.
