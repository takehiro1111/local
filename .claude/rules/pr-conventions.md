# PR の作成・更新

- PR 本文は対象リポジトリの `.github/PULL_REQUEST_TEMPLATE.md` に従う（`gh pr create` の前に必ず読む）
- 本文更新は現在の本文を取得して差分のみ反映する。全置換は禁止（ユーザーが編集した Related Issue 等を消さない）
- `gh pr edit` は Projects (classic) 廃止の GraphQL エラーで失敗することがあるため、本文更新は `gh api -X PATCH repos/{owner}/{repo}/pulls/{n} -F body=@file` を使う
