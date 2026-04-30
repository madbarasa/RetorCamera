# RetorCamera

![Version](https://img.shields.io/badge/version-0.2.3-blue.svg)
![Platform](https://img.shields.io/badge/platform-Web-brightgreen.svg)
![License](https://img.shields.io/badge/license-MIT-black.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

一个复古风格的网页拍立得应用：支持摄像头实时拍摄、图片上传、一键生成拍立得相纸，并可直接下载保存。

## 目录

- [项目亮点](#项目亮点)
- [在线体验与预览](#在线体验与预览)
- [快速开始](#快速开始)
- [配置说明](#配置说明)
- [项目结构](#项目结构)
- [兼容性](#兼容性)
- [开发计划](#开发计划)
- [贡献指南](#贡献指南)
- [许可证](#许可证)

## 项目亮点

- 实时摄像头拍摄与本地图片上传双模式。
- 拍照瞬间屏幕白闪、快门按压、闪光灯亮起三段式反馈。
- 自动生成带日期与装饰元素的拍立得风格相纸。
- 支持移动端与 PC 端自适配布局。
- 所有关键可调项集中在 `CONFIG` 配置代码块中，便于快速调参与调试。

## 在线体验与预览

- 本项目当前为本地静态页面形态，直接浏览器打开即可运行。
- 入口文件：`camera.html`

> 如果你计划部署到 GitHub Pages，可将该仓库设为静态站点并以该文件作为入口。

## 快速开始

```bash
# 1) 克隆仓库
git clone <your-repo-url>

# 2) 进入目录
cd RetorCamera

# 3) 直接在浏览器打开
camera.html
```

使用流程：

1. 点击镜头区域，上传本地图片（上传模式）。
2. 或允许摄像头权限，点击红色快门拍摄实时画面（相机模式）。
3. 在画廊查看新生成的拍立得，并点击“保存照片”下载。

## 配置说明

配置集中在 `camera.html` 的 `CONFIG` 代码块中：

- `appVersion`：应用版本号。
- `messages`：UI 文案（错误提示、iOS 保存提示等）。
- `effects.captureDelayMs`：快门触发后延迟拍摄时间。
- `effects.flashDurationMs`：屏幕白闪动画时长。
- `gallery.maxItems`：画廊最大保留张数。

通过调整上述配置，可快速完成功能调优，无需改动核心流程代码。

## 项目结构

```text
RetorCamera/
├─ camera.html        # 主应用（HTML + CSS + JS 单文件）
└─ README.md          # 项目说明文档
```

## 兼容性

- Chrome（推荐最新版）
- Edge（推荐最新版）
- Safari iOS（支持上传与拍摄，下载行为受系统策略影响）
- Android Chrome

说明：

- 首次使用摄像头需手动授权。
- iOS 上建议通过“长按图片”方式保存。

## 开发计划

- [ ] 增加更多相纸模板与滤镜预设
- [ ] 支持前后摄像头切换
- [ ] 增加批量导出与历史持久化能力
- [ ] 拆分单文件为模块化结构（便于维护）

## 贡献指南

欢迎提交 Issue 或 PR。建议在提交前确保：

- 功能可在移动端与 PC 端正常显示；
- 新增参数进入 `CONFIG` 配置块；
- 文档与版本号保持同步。

## 许可证

MIT License
