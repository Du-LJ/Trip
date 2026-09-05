# Trip Information Management

用于管理多个旅行目的地的静态手册站点。

## 当前结构

```text
Trip/
├── index.html                # 旅行总入口页
├── trips/
│   └── kansai/
│       └── index.html        # 关西旅行手册
└── README.md
```

后续新增目的地时，按下面的目录继续扩展即可：

```text
trips/<destination>/index.html
```

例如：

```text
trips/southeast-asia/index.html
```

## 当前已完成

- 根目录总入口页 `index.html`
- 关西页面 `trips/kansai/index.html`
- 单文件 HTML、零外部依赖、适合手机查看
- 结构上已支持未来新增更多目的地

## 本地预览

直接双击 HTML 文件即可预览，或在浏览器中打开：

- `index.html`
- `trips/kansai/index.html`

## GitHub Pages 部署

本项目适合直接使用 GitHub Pages 免费托管，无需服务器、无需额外付费。

### 第一次发布

1. 在本地仓库提交并推送代码

```bash
git add .
git commit -m "Initialize trip information site"
git push origin main
```

2. 打开 GitHub 仓库页面  
   仓库地址：`https://github.com/Du-LJ/Trip`

3. 进入：

```text
Settings → Pages
```

4. 在 `Build and deployment` 中设置：

- `Source`: `Deploy from a branch`
- `Branch`: `main`
- `Folder`: `/ (root)`

5. 保存后等待 GitHub Pages 发布完成

默认访问地址通常为：

```text
https://du-lj.github.io/Trip/
```

关西页面通常为：

```text
https://du-lj.github.io/Trip/trips/kansai/
```

### 后续更新

以后只要继续修改文件并执行：

```bash
git add .
git commit -m "Update trip content"
git push origin main
```

GitHub Pages 就会自动重新发布。

## 维护建议

- 行程细节尽量先在原始表格中补齐，再同步到页面
- 每个目的地继续保持单个 `index.html`，便于离线保存和分享
- 首页只负责列出目的地入口，不承载具体行程细节
