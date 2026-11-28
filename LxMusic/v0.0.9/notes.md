## 洛雪音乐·比亚迪车机版 v0.0.9

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
| `lx-music-mobile-v0.0.9-arm64-v8a.apk` | 14295422 | `7ff0b4cdb176a7c9ee49f858d42e07537de42c2bb5b66249f44ecd6663a94e5c` |
| `lx-music-mobile-v0.0.9-armeabi-v7a.apk` | 13288483 | `a388bed523291d1140c32985de7b3d536a7e52792b64310fbab9012855b3f67d` |
| `lx-music-mobile-v0.0.9-universal.apk` | 29293998 | `10af9d839e22b0f4cc7668d11cbbff0dff0eaa501f11854a12bef9759eeb605d` |
| `lx-music-mobile-v0.0.9-x86.apk` | 14739381 | `8d60448d1f2dca78708f25c72101adfcd9a973dc44ead99b18217f34d88fbc45` |
| `lx-music-mobile-v0.0.9-x86_64.apk` | 14619579 | `710d8db17715d1431b0842b75e5cce177909b5b7972f48b37067a8d32c5132eb` |

签名模式：`release`
