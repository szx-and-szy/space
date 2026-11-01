# space

个人空间单页，挂在 `space.szx-and-szy.com`。

纯静态，无依赖、无构建：一个 `index.html` 全包（CSS 内联，跟随系统深浅色）。

## 文件

- `index.html` — 页面本体
- `CNAME` — 自定义域名声明，值必须是 `space.szx-and-szy.com`（Pages 靠它绑定域名，删了会掉）

## 部署状态

GitHub Pages，`main` 分支根目录。

需要两个手动步骤（API 无法完成）：

1. **DNS**：在 `szx-and-szy.com` 的 DNS 里加一条记录
   - 类型 `CNAME`，主机记录 `space`，值 `szx-and-szy.github.io`
2. **开启 Pages**：仓库 `Settings → Pages → Build and deployment`
   - Source 选 `Deploy from a branch`，Branch 选 `main` / `/ (root)`，Save
   - 等证书签发后勾上 `Enforce HTTPS`

验证：`curl -I https://space.szx-and-szy.com` 返回 200 即通。
