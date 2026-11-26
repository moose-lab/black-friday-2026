# 2026 黑五必买高性价比清单 & Agent 自动省钱导航 (`moose-lab`)

> 按 **用途** 与 **性价比** 严选 13 款 2026 黑五实测史低产品，所有商品直达官方 / Amazon 购买页；并为 8 款入口较深、需切周期/填码/避坑的商品配套开源 **Agent Skill** (`black-friday-deal-navigator`)，让用户的 AI Agent 直接加载并自动定位最低价结账页。

- **GitHub 组织/仓库**: https://github.com/moose-lab
- **在线导航页 (GitHub Pages)**: 部署本仓库 `index.html` 后即可直接访问（开启 Settings → Pages → Deploy from `main` branch `/ (root)`）
- **Agent Skill 路径**: `skills/black-friday-deal-navigator/`
- **X (Twitter) 引流文案**: `X_POST_COPY.md`

## 快速部署到 GitHub Pages

```bash
git init
git add .
git commit -m "feat: launch 2026 Black Friday deals page & agent skill"
git branch -M main
git remote add origin https://github.com/moose-lab/black-friday-2026.git
git push -u origin main
```

随后进入 GitHub 仓库 **Settings → Pages → Source: Deploy from a branch → `main` / `(root)`**，保存后 1 分钟内即可生成公开访问网址。

## 2026 黑五必买清单（按性价比排序 · 直达购买页）

| 产品 | 用途 | 常规价 | 黑五价 | 优惠码 / 方式 | 入口类型 | 性价比 | 直达购买页 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Apple AirPods Pro 3 | 通勤降噪 / iOS / 心率监测 | $249 | **$149** (-40%) | Amazon 直降 | ⚡ 一键直达 | S级 (99) | [Amazon 直达](https://www.amazon.com/dp/B0FQFB8FMG) |
| JetBrains All Products Pack / IDEs | 全栈开发 / AI IDE | $299/年 | **~$179.40/年** (-40%) | `BF2026` (个人年付) | 🤖 深入口 Skill | S级 (98) | [JetBrains 商店](https://www.jetbrains.com/store/) |
| Hostinger Web Hosting & AI Builder | 独立开发建站 / 博客 | $585.12/4年 | **$1.99/月** (-85%) | 48月 + `COUPONSPAGE` ($1.89/月) | 🤖 深入口 Skill | S级 (97) | [Hostinger 黑五页](https://www.hostinger.com/black-friday) |
| Apple MacBook Air 15" M5 (16G/512G) | 移动办公 / 轻度开发 | $1,499 | **$1,199** (-20%) | Amazon 授权直降 | ⚡ 一键直达 | S级 (97) | [Amazon 直达](https://www.amazon.com/dp/B0GR114BV7) |
| Roborock Saros 20 扫拖机器人 | 全屋清洁 / 越障自集尘 | $1,599.99 | **$989.99** (-38%) | Amazon 直降省 $610 | ⚡ 一键直达 | S级 (96) | [Amazon 直达](https://www.amazon.com/dp/B0G64MM1HM) |
| NordVPN (2年 + 送3个月) | 全球高速加密 / 跨区办公 | $15.59/月 | **$2.99/月起** (-78%) | 黑五专页 2 年方案 | 🤖 深入口 Skill | S级 (96) | [NordVPN 黑五页](https://nordvpn.com/black-friday/) |
| Surfshark VPN / One (2年 + 3个月) | 无限设备 / 广告拦截 | $15.45/月 | **$2.49/月起** (-88%) | 黑五专页 24 个月 | 🤖 深入口 Skill | S级 (96) | [Surfshark 黑五页](https://surfshark.com/black-friday) |
| Sony WH-1000XM6 降噪耳机 | 深度专注 / 差旅降噪 | $459.99 | **$348.00** (-24%) | Sony 官网直降 | ⚡ 一键直达 | S级 (95) | [Sony 官网直达](https://electronics.sony.com/audio/headphones/headband/p/wh1000xm6-b) |
| DaVinci Resolve Studio (买断版) | 4K/8K 剪辑调色 / AI 降噪 | $295 | **~$236** (-20%) | 终身买断直降 | ⚡ 一键直达 | S级 (95) | [Blackmagic 官网](https://www.blackmagicdesign.com/products/davinciresolve/studio) |
| 1Password (个人 / 5人家庭版) | 密码管理 / SSH & Git 签名 | $3.99/月 | **$2.99/月** (-25%起) | 仅官网年付直购 | 🤖 深入口 Skill | A+级 (92) | [1Password 官网](https://1password.com/pricing/personal) |
| Cloudways 托管云服务器 | WordPress / Node.js 托管 | $14/月起 | **$2.80/月** (-80%) | 新号填 `BFCM802` | 🤖 深入口 Skill | A+级 (90) | [Cloudways 定价](https://www.cloudways.com/en/pricing.php) |
| Norton 360 Deluxe (5设备) | 防毒 / 反诈 / 50GB 云备份 | $124.99/年 | **$29.99/首年** (-76%) | 官网直达首年价 | 🤖 深入口 Skill | A级 (89) | [Norton 官网](https://us.norton.com/products/norton-360-deluxe) |
| Pictory AI 视频生成 (Pro 年付) | 文字转短视频 / 社媒运营 | $25+/月 | **年付 50% OFF** | `BLACKFRIYAYY50` | 🤖 深入口 Skill | A级 (88) | [Pictory 定价](https://pictory.ai/pricing/) |

## 让你的 AI Agent 自动走深入口省钱

将仓库中的 `skills/black-friday-deal-navigator/` 导入你的 AI Agent，然后直接发指令：

> “加载 black-friday-deal-navigator，帮我用 2026 黑五最低价买 JetBrains All Products Pack（切个人年付并填码 BF2026），核对好总价后停在付款页等我确认。”
