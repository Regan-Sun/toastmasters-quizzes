# 测评中心

头马风格的两项在线测评，静态站点，无后端依赖。

## 线上地址

- 站点首页：https://regan-sun.github.io/toastmasters-quizzes/
- CSI 沟通风格测评：https://regan-sun.github.io/toastmasters-quizzes/csi-deploy.html
- 领导风格测评：https://regan-sun.github.io/toastmasters-quizzes/leadership-quiz.html

## 内容

| 测评 | 题量 | 结果维度 |
|---|---|---|
| CSI 沟通风格测评 | 12 题 | 4 种风格（direct / interactive / supportive / analytical）|
| 领导风格测评 | 48 题 | 8 种风格（官僚 / 权威 / 创新 / 带头 / 民主 / 亲和 / 教练 / 无私）|

所有作答与计分均在浏览器本地完成，**不会上传任何数据**。

## 部署

`.github/workflows/deploy.yml` 配置了 GitHub Actions：推送到 `main` 即自动发布到 GitHub Pages。

```bash
git add -A && git commit -m "更新内容" && git push
```

也可在 Actions 页面手动触发。

## 资源说明

`assets/` 目录用于放自定义 logo。CSI 页面引用 `assets/logo.png`，
该文件不存在时会自动隐藏 logo 区域（页面已内置 `onerror` 兜底），不影响使用。

分享海报功能依赖 CDN 上的 html2canvas（首次打开需联网加载）。