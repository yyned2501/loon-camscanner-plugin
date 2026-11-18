# CamScanner Loon 规则归档

本仓库仅归档一条**已下架**的 Loon 插件规则片段，作留档备份之用。不维护、不扩展原功能。

## 规则文件

`camscanner.loon` —— 用户提供的原始单行规则，**逐字保留，未作任何改动**：

```loon
response if ${url} ~= /https:\/\/(api|api-cs)\.intsig\.net\/purchase\/cs\/query_property\?/i then script("https://raw.githubusercontent.com/NobyDa/Script/master/Surge/JS/CamScanner.js") with tag="扫描全能王", requires_body=true
```

## 依赖与说明

- 这是一条 Loon `response` 改写规则：匹配扫描全能王（CamScanner）购买接口的 `query_property` 响应。
- 规则通过 `script(...)` 调用外部公开脚本：`https://raw.githubusercontent.com/NobyDa/Script/master/Surge/JS/CamScanner.js`（由 NobyDa 维护，非本仓库内容）。
- 本仓库既不包含也不修改该 JS 脚本，仅引用其公开 URL。
- **未经验证**：未在实际环境测试过该规则，不保证其当前仍可用；归档目的仅为保存原始片段。
- 不含任何凭据或账号信息。
