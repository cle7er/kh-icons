# KlausHome 图标库

家庭影院（Emby / DrivEmby 系播放器）自定义图标库，收录 KH 系列徽记，含经典款与无外圆新方向款；每款含深底版与透明底版，均为 512×512 PNG。

## 图标清单

| 匹配键 | 款式 | 深底版 | 透明底版 |
| --- | --- | --- | --- |
| `kh` / `emby` / `KlausHome` | G 圆形胶片徽记（默认） | `icons/kh.png` | `icons/kh-transparent.png` |
| `kh-film` | C 胶片横条 | `icons/kh-film.png` | `icons/kh-film-transparent.png` |
| `kh-seal` | D 叠方印章 | `icons/kh-seal.png` | `icons/kh-seal-transparent.png` |
| `kh-ring` | E 圆环徽章 | `icons/kh-ring.png` | `icons/kh-ring-transparent.png` |
| `kh-circle` | F 正圆胶片徽记 | `icons/kh-circle.png` | `icons/kh-circle-transparent.png` |
| `kh-wordmark` | 新方向·纯字标（无外框） | `icons/kh-wordmark.png` | `icons/kh-wordmark-transparent.png` / `icons/kh-wordmark-dark-transparent.png` |
| `kh-strip` | 新方向·胶片横条（无外框） | `icons/kh-strip.png` | `icons/kh-strip-transparent.png` / `icons/kh-strip-dark-transparent.png` |

## 目录结构

```
kh-icons/
├── emby-icons.json          # 图标库清单（播放器填这个文件的 raw 直链）
├── README.md
└── icons/                   # 各款深底/透明底，512×512 PNG
```

## 播放器怎么填

图标库 URL（JSON raw 直链）：

```
https://raw.githubusercontent.com/cle7er/kh-icons/main/emby-icons.json
```

在播放器「添加图标库 → URL」粘贴上面这条即可。

## 图标匹配规则

JSON 里 `name` 是匹配键：播放器用媒体库名称 / 服务器名称匹配 `name`，命中后取对应 `url` 的图标。
需要给别的分类加图标时，在 `icons/` 放图，并在 JSON 的 `icons` 数组追加一条：

```json
{ "name": "分类名", "url": "https://raw.githubusercontent.com/cle7er/kh-icons/main/icons/xxx.png" }
```

## 版本说明

- 新方向两款（wordmark / strip）不套外圆、不画闭合边框，金色为深古铜金。
- 透明底各有两套：`-transparent` 为米白字母，贴深色界面用；`-dark-transparent` 为深墨蓝字母，贴浅色背景用。
- 深底版为米白字母垫深墨蓝底，深色界面直接用。
- raw 链接依赖 GitHub 域名访问；私有仓库不能直接用 raw 直链。
