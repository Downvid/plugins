# DownVid 插件索引

这里是 DownVid 的**插件索引**：一份 `index.json`，列出被收录的第三方解析插件。

应用内「设置 → 插件」会读取本仓库的 `index.json` 显示列表。

## 重要：本仓库不托管插件代码

索引里只有 `owner/repo` 指向作者自己的仓库。插件代码、更新与坏掉了的修复，
都由作者负责。**收录不等于背书**功能、可用性或合法性。

## 提交收录

开一个 Issue，附上：

1. 插件仓库地址（GitHub，**公开**）
2. 一句话说明它支持哪些站点
3. 插件目录里 `plugin.json` 的内容

## 收录条件

只审「能不能装、会不会伤人」，不审功能强弱：

- [ ] `plugin.json` 合法，`playback` 为 `downvid-parser`
- [ ] `permissions.network` 是最小集合，不写 `*`
- [ ] 没有明显的数据外传：不把 Cookie / 设置 / 历史发往与解析无关的域名
- [ ] 仓库公开、可追溯，有可读源码（不接受只有混淆产物）
- [ ] `id` 与仓库内的插件目录名一致，且不与已有插件重复

## 下架

出现恶意代码、窃取凭据或明显的数据外传，会从 `index.json` 移除。
下架只影响索引，不会删除用户已安装的文件。

移除记录留在 `removed.json`，写清原因与日期——用户和作者都应该能看到
「为什么没了」，而不是插件静静消失。

## 协议与字段

见 DownVid 主仓库的 [`docs/dev/plugins.md`](https://github.com/Downvid/downvid/blob/main/docs/dev/plugins.md)。
`index.json` 的字段约束见 [`index.schema.json`](./index.schema.json)。
