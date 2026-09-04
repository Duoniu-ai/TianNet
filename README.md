# TianNet 天网互联 — OSINT Tree PoC

这是 TianNet 的一个**测试版 UI / 数据结构 PoC**，用于验证 OSINT Framework 风格的分类树、D3.js 交互和 GitHub Pages 静态部署。

> 当前数据是测试用 fixture，不代表 TianNet 正式知识网络数据，也不是 OSINT Framework 的完整镜像。

## 功能

- D3.js 自上而下树状展示
- 分类节点展开 / 收起
- 工具节点点击后新标签页打开
- 顶部搜索并定位匹配项
- 滚轮缩放、拖拽平移
- 工具链接悬浮提示

## 文件

```text
index.html   # 页面与 D3.js Tree 逻辑
arf.json     # 测试分类与工具数据
README.md    # 项目说明
```

## 本地测试

在项目目录运行任意静态 HTTP 服务，例如：

```bash
python3 -m http.server 8000
```

然后打开：

```text
http://localhost:8000/
```

不要直接使用 `file://` 打开 `index.html`，因为浏览器可能阻止 `d3.json()` 加载本地 JSON。

## GitHub Pages

仓库：

https://github.com/Duoniu-ai/TianNet

当前分支：`main`

在 GitHub 中进入：

`Settings → Pages → Deploy from a branch → main → / (root)`

保存后，GitHub Pages 会从 `main` 分支根目录发布。

## 数据来源说明

`arf.json` 参考 OSINT Framework 的分类与资源组织思路，并加入少量代表性工具作为测试数据。

参考项目：

- https://osintframework.com/
- https://github.com/lockfale/OSINT-Framework

## 标记

| 标记 | 含义 |
|---|---|
| `(T)` | 需要本地安装 / 运行的工具 |
| `(D)` | Google Dork / 搜索语法 |
| `(R)` | 通常需要注册账号 |
| `(M)` | 需要手动编辑 URL |

## 当前定位

本仓库当前只用于测试 TianNet 的可视化 Tree / 数据文件组织方式。

后续是否演进为正式 TianNet Knowledge Network、是否接入 SiteIntel / DUONIU / Mangzhuo，不属于本 PoC 的范围。
