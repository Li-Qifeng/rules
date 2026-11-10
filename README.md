# Rules Collection

个人代理分流规则集，适用于 Loon、Surge、Shadowrocket 等 iOS / macOS 代理客户端。

---

## 规则列表

### Siri & Apple Intelligence

专为国区/改区 iOS 体验完整 Apple Intelligence 与 Siri 拟物玻璃球/云端模型设计的精准分流规则集：
- 覆盖 Siri、Dictation 听写语音核心网关
- 覆盖 Private Cloud Compute (PCC) 与 OHTTP Relay 链路
- 覆盖 Private Relay 鉴权与 CloudKit 状态探测
- 防地区检测回退

#### 1. 远程规则订阅（推荐，用于 Loon / Surge）

* **GitHub Raw 官方直连**：
  ```text
  https://raw.githubusercontent.com/Li-Qifeng/rules/main/siri.list
  ```

* **国内 CDN 加速（免翻墙直连，蜂窝网络更新推荐）**：
  ```text
  https://cdn.jsdelivr.net/gh/Li-Qifeng/rules@main/siri.list
  ```

#### 2. Loon 引用示例

在 Loon 配置文件的 `[Remote Rule]` 模块添加：
```ini
[Remote Rule]
https://cdn.jsdelivr.net/gh/Li-Qifeng/rules@main/siri.list, policy=节点选择, tag=Apple Siri, enabled=true
```

> **提示**：若要在本地 `[Rule]` 中直接写入，请使用自带策略的 `siri-full.list`。
