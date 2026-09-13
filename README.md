# A7 · Stairwell 楼梯间策展

以「楼梯间」为主题的策展项目：一个网页展示卡片 + 一份调研文档与图片资料库。

## 项目结构

```
.
├── index.html                  # 楼梯间网页卡片主页面
├── stairwell_index_v3.html     # 网页卡片 v3 版本（存档）
├── server.js                   # 本地静态服务器
├── package.json
├── img/                        # 网页使用的图片素材
├── stairs-preview/             # 楼梯 3D 预览页面（demo / index / stairwell）
├── A7-excel-9.13/
│   ├── 楼梯间调研文档 9.13.xlsx      # 调研文档（完整版，334MB，Git LFS）
│   └── 楼梯间图片-webp格式/          # 162 张调研图片（webp）
└── README.md
```

## 快速开始

无需安装依赖，`server.js` 是一个零依赖的极简静态服务器（Node.js 内置模块实现）：

```bash
node server.js                # 默认 http://127.0.0.1:7100/
node server.js --port 8000    # 自定义端口
node server.js --host 0.0.0.0 # 允许局域网访问
```

浏览器打开终端中显示的地址即可查看网页卡片。

## 内容说明

- **网页卡片**：`index.html` 为入口，展示楼梯间主题策展内容，图片素材位于 `img/`
- **调研文档**：`A7-excel-9.13/楼梯间调研文档 9.13.xlsx`，收录楼梯间相关电影、建筑、艺术等条目（单个文件超过 100MB，通过 Git LFS 存储，网页端点击文件后通过 LFS 链接下载）
- **图片资料库**：`A7-excel-9.13/楼梯间图片-webp格式/`，162 张 webp 图片，文件名前缀对应调研文档中的条目编号（a- 电影 / b- 建筑 / c- 艺术 / d- 其他）

## Git LFS

本仓库使用 Git LFS 管理大文件（`*.xlsx`）。克隆后如需检出完整文档：

```bash
git lfs install
git lfs pull
```
