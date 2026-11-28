## 洛雪音乐·比亚迪车机版 v0.0.8

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
| `lx-music-mobile-v0.0.8-arm64-v8a.apk` | 14290795 | `06798f7a9b56c4a7fc4b39f5d947c2409667161c5555bbe6661660eca8bd758e` |
| `lx-music-mobile-v0.0.8-armeabi-v7a.apk` | 13283858 | `0dca66d5bdf57992912bfe1e9674a86e026be47a171769d76a5da2bae5ba098d` |
| `lx-music-mobile-v0.0.8-universal.apk` | 29289359 | `7889c41da0f191916f996989fa7ebbc2f2146be85581b5b437c34ca524aedc48` |
| `lx-music-mobile-v0.0.8-x86.apk` | 14734745 | `8e76b0f0b7bfaad2264616e7813c4e4539e81914313b6db4ee5081ca679ca0d1` |
| `lx-music-mobile-v0.0.8-x86_64.apk` | 14614947 | `99c78662822a2a2daad67dd326927c4e3a2160b795c1a48f8388e5adf6797510` |

签名模式：`release`
