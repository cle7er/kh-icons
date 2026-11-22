# KlausHome 图标库

家庭影院（Emby / DrivEmby 系播放器）自定义图标库，收录 KH 圆形胶片徽记。

## 目录结构

```
kh-icons/
├── emby-icons.json          # 图标库清单（播放器填这个文件的 raw 直链）
└── icons/
    ├── kh-logo.png          # 深墨蓝底圆形图标 512×512
    └── kh-logo-transparent.png  # 透明底圆形图标 512×512
```

## 部署到 GitHub 后怎么填

1. 把本仓库推到 GitHub **公开仓库**，分支名 `main`。
2. 打开 `emby-icons.json`，把里面的 `REPLACE_USER` 换成你的 GitHub 用户名，`REPLACE_REPO` 换成仓库名。
3. 图标库 URL 填 JSON 的 raw 直链，格式：

```
https://raw.githubusercontent.com/<用户名>/<仓库名>/main/emby-icons.json
```

4. 播放器「添加图标库 → URL」粘贴上面这条链接即可。

## 图标匹配规则

JSON 里 `name` 是匹配键：播放器会用媒体库名称 / 服务器名称去匹配 `name`，命中后取对应 `url` 的图标。
需要给别的分类加图标时，在 `icons` 数组里追加一条：

```json
{ "name": "分类名", "url": "https://raw.githubusercontent.com/<用户名>/<仓库名>/main/icons/xxx.png" }
```

## 备注

- 透明底版本字母为米白色，贴浅色背景对比偏弱；深色界面优先用 `kh-logo.png`。
- raw 链接依赖 GitHub 域名访问；私有仓库不能直接用 raw 直链。
