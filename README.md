# muse-qx-rules

Meta Muse AI 的 Quantumult X 分流规则订阅。

Converted from the Loon rule set at [juner922/muse-loon-rules](https://github.com/juner922/muse-loon-rules).

## 订阅方式

在 Quantumult X「分流规则」中添加远程规则，URL 任选其一：

- GitHub Raw：`https://raw.githubusercontent.com/lilBam2331/muse-qx-rules/main/MuseAI_QX.list`
- jsDelivr CDN（国内访问更快）：`https://cdn.jsdelivr.net/gh/lilBam2331/muse-qx-rules@main/MuseAI_QX.list`

添加时将 `force-policy` 指向你的美国节点策略组，例如：

```
https://raw.githubusercontent.com/lilBam2331/muse-qx-rules/main/MuseAI_QX.list, tag=MuseAI, force-policy=美国节点, update-interval=86400, opt-parser=false, enabled=true
```

也可以直接复制 `MuseAI_QX.list` 的内容到 `[filter_local]` 中（放在 `final` 规则之前），并按需把行尾的 `proxy` 批量替换为你的策略组名。

## 规则说明

- `MuseAI_QX.list`：共 24 条规则。Muse App 核心域名（`muse.ai` / `metaaivm.com` / `meta.com` 等）+ Meta 账号与社交基础设施（Facebook / Instagram / WhatsApp / fbcdn 等）
- 域名来源：Meta Muse 客户端二进制逆向分析（mahdi-salmanzade/meta-muse-teardown），经社区实测交叉核实

## 注意事项

Muse 有地区限制：即使域名全部走代理，若出口 IP 不是美区原生/家宽 IP，仍会提示“尚未在你的国家或地区开放”。请使用美区家宽节点。
