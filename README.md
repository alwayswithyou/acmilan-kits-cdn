# AC Milan Kit CDN

AC 米兰 2021-22 ~ 2026-27 赛季球衣图鉴配图（22 张），经 jsDelivr CDN 分发。

## 链接格式

```
https://cdn.jsdelivr.net/gh/<你的用户名>/acmilan-kits-cdn@v1/images/01-2122-away.jpg
```

国内访问慢时，把 `cdn.jsdelivr.net` 换成以下任一备用域名即可，路径不变：

- `fastly.jsdelivr.net`（推荐，国内节点多）
- `gcore.jsdelivr.net`
- `testingcf.jsdelivr.net`

## 注意事项

1. 仓库必须为 **Public**，jsDelivr 才能访问私有仓库之外的资源
2. 打 tag 后链接才有 `@v1` 这个固定版本；不打 tag 则去掉 `@v1`，用默认分支
3. jsDelivr 有缓存，push 后首次访问可能需要 1-5 分钟生效
4. 单文件上限 20MB，本仓库单图最大约 190KB

## 图片清单

带 `-wide` 后缀的是横版图，适合做封面（建议裁成 2.35:1）。

### 目录与 tag 对应

| 目录 | 内容 | tag | 用途 |
|---|---|---|---|
| `images/` | 22 张赛季球衣图 | `v1` / `v2` | 《AC米兰球衣图鉴》正文 |
| `gallery/` | 39 张交互图鉴压缩图 | `v2` | `index.html` Pages 版 |
| `collab/` | 12 张联名款球衣 | `v2` | `collab.html` Pages 版 |
| `opel/` | 18 张欧宝时期配图 + `00-cover.jpg`（900×383 封面） | `v3` | 《欧宝时期AC米兰队服》公众号版外链 |

`opel/` 图片按正文出现顺序编号（`01`~`18`），与《欧宝时期AC米兰队服_头条手动插图版.md》里的
`【配图 NN】` 标记一一对应。

