# Shadowrocket 分流规则（适用于中国大陆）

该规则集旨在实现以下目标：

- 中国大陆常见网站和 APP **直连**
- 海外服务（如 TikTok、YouTube、Telegram 等）**分国家走代理**
- 自动引用广告屏蔽、Apple、CN 域名/IP 等规则集

## ✨ 使用说明

1. 打开 Shadowrocket
2. 导入配置：配置 → 规则 → 从链接下载
3. 使用以下链接导入：
```
https://raw.githubusercontent.com/xunchang20808/shadowrocket-rules/main/rules.conf
```

> 请将 `your_github_id` 替换为你的 GitHub 用户名。

## 🧩 包含的规则

- ✅ 国内域名直连（如 bilibili、淘宝、抖音等）
- 🌐 TikTok / YouTube / Instagram → 美区代理
- 📦 Telegram → 港区代理
- 🧹 广告屏蔽（引用 ACL4SSR）
- 🍎 Apple 服务直连
- 🌏 CN IP 网段直连

## 🛠 维护建议

- 每周检查一次 geosite/geolocation 规则是否过期
- 可使用 GitHub Actions 定时更新

## 🧪 节点命名建议

| 节点名称       | 功能说明           |
|----------------|--------------------|
| Proxy_US       | TikTok/YouTube 等美区应用 |
| Proxy_JP       | 日本应用（如 LINE） |
| Proxy_HK       | Telegram 等低延迟服务 |
| Proxy_Default  | 默认海外代理       |
| DIRECT         | 直连本地网络       |
| REJECT         | 拒绝连接（如广告） |

## 📁 项目结构

```
shadowrocket-rules/
├── rules.conf          # 主规则文件
└── RULE-SET/           # 可选子规则（引用）
```

## 📢 免责声明

仅用于学习交流，请勿用于非法用途。
