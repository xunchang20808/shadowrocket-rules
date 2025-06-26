# 🇨🇳 Shadowrocket 分流规则（适用于中国大陆）

本项目提供适用于 **中国大陆用户** 的 Shadowrocket 分流规则，具备以下功能：

- ✅ **中国大陆网站 / APP 直连**
- 🌐 **海外服务按国家分流（如 TikTok / YouTube / Telegram）**
- 🧹 **广告拦截（自动引用 ACL4SSR）**
- 🍎 **Apple 服务直连**
- 🌏 **国内 IP 网段直连**

---

## ✨ 使用说明

1. 打开 Shadowrocket
2. 前往「配置」→「规则」→「从链接下载」
3. 粘贴以下订阅链接导入：

```
https://raw.githubusercontent.com/xunchang20808/shadowrocket-rules/main/rules.conf
```

> 📌 建议开启 Shadowrocket 的「策略分流」功能，以便规则生效

---

## 🧩 已包含的规则

| 类别       | 内容                                 |
|------------|--------------------------------------|
| 国内直连   | `.cn` 域名、bilibili、抖音、淘宝等常用服务 |
| 广告拦截   | 引用 [ACL4SSR/Advertising.list](https://github.com/ACL4SSR/ACL4SSR) |
| Apple 服务 | 使用 [Apple.list](https://github.com/ACL4SSR/ACL4SSR) 直连 |
| Telegram   | 港区节点分流（如 Proxy_HK）            |
| TikTok     | 美区节点分流（如 Proxy_US）            |
| YouTube    | 美区节点分流（如 Proxy_US）            |
| Instagram  | 美区节点分流                          |
| CN IP      | IP 段自动匹配直连（geoip:cn）          |

---

## 📁 项目结构

```
shadowrocket-rules/
├── rules.conf              # 主规则文件
├── RULE-SET/               # 子规则文件夹（广告、Apple）
└── .github/workflows/      # 自动更新 GitHub Actions
```

---

## 🧪 节点命名建议（请与配置中策略组对应）

| 节点名称       | 功能说明                     |
|----------------|------------------------------|
| Proxy_US       | TikTok / YouTube / Instagram |
| Proxy_HK       | Telegram / 港澳服务           |
| Proxy_JP       | 日本地区服务（如 LINE）       |
| Proxy_Default  | 其他未匹配走此代理           |
| DIRECT         | 本地直连                     |
| REJECT         | 拒绝连接（如广告）           |

---

## 🛠 自动维护说明

- 使用 GitHub Actions 每周一自动更新：
  - Advertising.list
  - Apple.list
- 可手动触发更新或自定义规则

---

## 📢 免责声明

本项目仅用于技术学习与研究，请勿用于商业用途或违反当地法律政策。
