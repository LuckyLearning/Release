## 洛雪音乐·比亚迪车机版 v0.0.7

首个车机适配版本，基于上游 LX Music v1.9.2（同步基线 `0669d1b`）。

### 本版内容

- **车机横屏界面**：22 个车机组件 + 夜曲/白昼双主题 + Inter 字体，1920×1080 设计基准自适应缩放；手机竖屏界面保持上游原样。
- **三七分屏**：声明 `BYD_SUPPORT_SPLIT_ACTIVITY`（API≥32 生效）+ `resizeableActivity`，可在比亚迪车机 7 分屏中与导航共存。
- **悬浮歌词增强**：多屏识别与投射选择、背景色/圆角/边框色/边框宽/字间距/字体可调（滑块）、描边可读性、前台服务保活。

### 安装说明

- 首次安装请先卸载已安装的洛雪音乐（签名不同，无法覆盖安装）。
- 若已安装上游正式版，同样需卸载后再装本包。

### 文件校验

| 文件 | 大小 | SHA-256 |
| --- | --- | --- |
| `lx-music-mobile-v0.0.7-arm64-v8a.apk` | 14289136 | `240f92ecbf0e40ebdc3354ed1b5d23223e7c6b6dff6d662bfb1007ef7b7a629e` |
| `lx-music-mobile-v0.0.7-armeabi-v7a.apk` | 13282196 | `031ca3e9ab07107700213c9154800db493764a1f1b0cac67a41696cce32890a5` |
| `lx-music-mobile-v0.0.7-universal.apk` | 29287686 | `b16b8e352388b577294d99dbbb3d24e8fb457962ee2151aa2f136980933b3781` |
| `lx-music-mobile-v0.0.7-x86.apk` | 14733088 | `43387e70f5892410cd930c724d2cedc8a45c438d81b83633e6b9a1aa72d52b69` |
| `lx-music-mobile-v0.0.7-x86_64.apk` | 14613288 | `3d9ade7e014f2466311325f74b09eb7ab89ef2ccc4ced1e5b9facb0a84310550` |

签名模式：`release`
