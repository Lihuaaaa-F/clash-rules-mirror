# clash-rules-mirror

每日自动镜像 [Loyalsoldier/clash-rules](https://github.com/Loyalsoldier/clash-rules) 的规则文件，供 Clash Verge / mihomo 的 `rule-providers` 引用。

- **更新方式**：GitHub Actions 每日 UTC 00:30（北京时间 08:30）定时同步；上游无变更则不提交。也支持在 Actions 页手动触发（workflow_dispatch）。
- **数据来源**：上游 `release` 分支，本仓库不做任何修改，仅做快照备份。
- **引用示例**：
  ```
  https://raw.githubusercontent.com/Lihuaaaa-F/clash-rules-mirror/main/rules/proxy.txt
  ```

## 文件清单

`reject` `icloud` `apple` `google` `proxy` `direct` `private` `gfw` `tld-not-cn` `telegramcidr` `cncidr` `lancidr` `applications`

均为 YAML payload 格式（`.txt` 扩展名），`behavior` 对应关系：域名类用 `domain`，IP 段类（telegramcidr/cncidr/lancidr）用 `ipcidr`，applications 用 `classical`。

## 注意

- 若仓库 60 天无活动，GitHub 会自动停用定时工作流；本工作流每日自动提交，正常情况下不会触发。
- 定时任务可能有几分钟延迟，属 GitHub 正常现象。
