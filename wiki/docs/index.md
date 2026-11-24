# Gozjaro Linux

Gozjaro 是一个从 LFS 自举、用自家包管理器 **gozpak** 管理的独立 Linux 发行版。
工具链、内核、包，都从源码一路搓上来。

!!! warning "状态：开发中"
    gozpak 的 Rust 版本仍在推进（M2b），`remove` 等命令尚未完成。日常主力机请谨慎。

## 特点

- **gozpak**：KISS 起家，正在用 Rust 重写。一个包 = 一个 `recipe.toml`
- **签名的二进制仓库**：`.gpkg`（tar.zst）托管在 GitHub Releases，索引用 ed25519 签名，每次 `sync` 都校验
- **依赖解析**：版本约束（`zlib>=1.3`）、epoch、`provides` / `conflicts`
- **x86_64**，从 LFS 自举

## 快速开始

```sh
gozpak sync          # 同步并校验仓库索引
gozpak get curl      # 安装 curl 及其依赖
gozpak list          # 列出已安装的包
gozpak search 'zl*'  # 搜索配方
```

## 文档（待写）

| 我想…… | 页面 |
|---|---|
| 装系统 | 安装指南 |
| 装软件、管理包 | gozpak 使用 |
| 自己打包 | 编写 recipe.toml |
| 从零构建 Gozjaro | Bootstrap |
| 内核 | 内核 |
| 桌面与壁纸 | 桌面环境 |

## 参与

- 源码：[github.com/Gozjaro](https://github.com/Gozjaro)
- 包管理器：[gozpak](https://github.com/Gozjaro/gozpak) · 官方仓库：[gozjaro-repo](https://github.com/Gozjaro/gozjaro-repo)
- 讨论：[Gozjaro/discussions](https://github.com/Gozjaro/discussions)

发现写错了？点页面右上角的编辑按钮直接提 PR。
