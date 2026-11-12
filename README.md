# kkmihomo-rules

Clash Verge Rev 全局扩展脚本和 RouteKit 自定义规则备份。此仓库不包含机场节点或订阅链接。

## 使用

选择精品机场的 Clash/Mihomo 远程订阅作为当前配置，把 `Clash-Verge-Rev-RouteKit-Premium-Primary-v4.js` 粘贴到全局扩展脚本，并仅在本机填写脚本顶部的 `ECONOMY_SUBSCRIPTION_URL`。不要将填写过订阅链接的脚本提交到仓库。

## 规则来源

- 脚本框架借鉴 [skullvek/Mihomo-RouteKit](https://github.com/skullvek/Mihomo-RouteKit)，起点为提交 [760a342](https://github.com/skullvek/Mihomo-RouteKit/commit/760a342e91568167ee608a6fb4a6b721b65f5a76)。本仓库的脚本后续独立维护，不会自动同步上游脚本改动。
- `BM_*` 服务规则和 `ChinaMax` 从 [blackmatrix7/ios_rule_script](https://github.com/blackmatrix7/ios_rule_script) 的 `master` 分支下载。
- 基础地理和服务规则从 [MetaCubeX/meta-rules-dat](https://github.com/MetaCubeX/meta-rules-dat) 的 `meta` 分支下载。
- `SKULL_CustomDirect`、`SKULL_CustomProxy`、`SKULL_FakeIPFilter` 目前仍从 RouteKit 的 `main/rules/` 下载。脚本设置的规则更新间隔为 86400 秒；实际生效取决于客户端运行、下载成功和缓存。

## RouteKit 规则备份

`rules/direct.list`、`rules/proxy.list`、`rules/fake-ip-filter.list` 是 RouteKit 提交 [760a342](https://github.com/skullvek/Mihomo-RouteKit/commit/760a342e91568167ee608a6fb4a6b721b65f5a76) 的副本，分别用于直连补丁、代理补丁和 Fake-IP 排除。它们目前**仅作备份**；运行中的脚本仍读取上游 RouteKit。

此仓库是私有仓库，Mihomo 无法直接匿名读取这里的 Raw 文件。若上游文件被删除或不可用，需要把备份规则内置到脚本，或迁移到可供客户端读取的规则地址，然后重新测试配置；仅保存备份不会自动切换下载源。
