# Tab Out - Aikoin Custom

这是 Aikoin 基于原版 **Tab Out** 改造的 Chrome 新标签页插件。它会把当前打开的标签页按域名分组展示，并提供一键关闭、重复标签清理、稍后保存等功能。

## 原作者与原仓库

本项目基于 Zara 的开源项目二次修改：

- 原作者：Zara
- 原仓库：[https://github.com/zarazhangrui/tab-out](https://github.com/zarazhangrui/tab-out)
- 原项目 License：MIT

本仓库是个人改版，不是原项目的官方版本。原始创意、Chrome extension 结构和基础功能来自上面的原仓库；这个版本主要调整了视觉风格、字体、问候语、主题素材和部分动效。

## 这个版本改了什么

- 换成薄荷绿小羊涂鸦风视觉。
- 中文为主的界面字体改为 `Noto Sans SC`。
- 英文、数字、状态标签使用 `Roboto Mono`，让中英混排更有秩序。
- 顶部问候改成小羊口吻，例如 `人，晚上好。`
- 加粗顶部问候，让它在页面里更醒目。
- 优化卡片入场动画，避免左侧列看起来加载更慢。
- 增加个人改版的打包文件：`dist/tab-out-extension.zip`。

## 功能

- 按域名分组查看所有打开的标签页。
- 首页类标签页，例如 Gmail、X、YouTube、GitHub，可以单独归组。
- 点击标签标题可以直接跳转到对应 Chrome 标签页。
- 一键关闭某个分组里的所有标签页。
- 检测重复标签，并支持一键关闭重复项。
- 将标签保存到稍后列表。
- 所有数据都保存在本地 `chrome.storage.local`，不需要服务器或账号。

## 安装

### 方法一：加载源码目录

```bash
git clone https://github.com/Aikoin/tab-out.git
```

然后：

1. 打开 Chrome，进入 `chrome://extensions`
2. 打开右上角 **Developer mode**
3. 点击 **Load unpacked**
4. 选择仓库里的 `extension/` 文件夹
5. 打开新标签页

### 方法二：使用打包文件

仓库里提供了打包好的扩展文件：

```text
dist/tab-out-extension.zip
```

解压后，在 `chrome://extensions` 里用 **Load unpacked** 选择解压出来的扩展目录。

## 打包

如果改完代码后需要重新生成 zip：

```bash
cd extension
zip -r ../dist/tab-out-extension.zip . -x '*.DS_Store'
```

## 技术栈

| 部分 | 实现 |
| --- | --- |
| Chrome extension | Manifest V3 |
| 数据存储 | `chrome.storage.local` |
| 声音 | Web Audio API |
| 动效 | CSS transitions + JS confetti particles |

## License

MIT. 请同时参考原项目的 License 和 attribution：

[https://github.com/zarazhangrui/tab-out](https://github.com/zarazhangrui/tab-out)
