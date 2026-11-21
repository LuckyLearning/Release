# Release

本仓库用于分发各软件的安装包。目录按 **软件名 / 版本号** 组织，每个软件**只保留最近 5 个版本**，更旧的版本在发布新版本时自动清理。

> 本文件由发布流水线自动生成（`scripts/gen-release-manifest.py`），**请勿手工修改** —— 下次发版会被覆盖。

## 目录结构

```
Release/
├─ README.md                       # 本文件（自动生成）
├─ AnyLyric/
│  ├─ latest.json
│  ├─ v0.2.30/
│  ├─ v0.2.29/
│  ├─ v0.2.28/
│  ├─ v0.2.27/
│  ├─ v0.2.26/
│  └─ …（最多 5 个版本目录）
├─ GlucoNote/
│  ├─ latest.json
│  ├─ v1.2.10/
│  ├─ v1.2.9/
│  ├─ v1.2.8/
│  ├─ v1.2.7/
│  ├─ v1.2.6/
│  └─ …（最多 5 个版本目录）
├─ LxMusic/
│  ├─ latest.json
│  ├─ v0.0.11/
│  ├─ v0.0.10/
│  ├─ v0.0.9/
│  ├─ v0.0.8/
│  ├─ v0.0.7/
│  └─ …（最多 5 个版本目录）
├─ WindTone/
│  ├─ latest.json
│  ├─ v1.2.61/
│  ├─ v1.2.60/
│  ├─ v1.2.59/
│  ├─ v1.2.58/
│  ├─ v1.2.57/
│  └─ …（最多 5 个版本目录）
```

命名约定（固定，便于机器解析）：

| 项 | 规则 | 示例 |
|---|---|---|
| 软件目录 | 英文名，驼峰 | `LxMusic` |
| 版本目录 | `v` + 语义化版本 | `v0.2.30` |
| 安装包 | `<软件>-v<版本>-<abi>.apk` | `lx-music-mobile-v0.2.30-arm64-v8a.apk` |
| 元数据 | 每个软件根目录一份 `latest.json` | `LxMusic/latest.json` |

## 软件列表

| 软件 | 目录 | 最新版本 | 在库版本 |
|---|---|---|---|
| AnyLyric | [`AnyLyric/`](AnyLyric/) | [v0.2.30](AnyLyric/v0.2.30/) | v0.2.30、v0.2.29、v0.2.28、v0.2.27、v0.2.26 |
| GlucoNote | [`GlucoNote/`](GlucoNote/) | [v1.2.10](GlucoNote/v1.2.10/) | v1.2.10、v1.2.9、v1.2.8、v1.2.7、v1.2.6 |
| 洛雪音乐·比亚迪车机版（LX Music 车机适配（三七分屏 / 悬浮歌词）） | [`LxMusic/`](LxMusic/) | [v0.0.11](LxMusic/v0.0.11/) | v0.0.11、v0.0.10、v0.0.9、v0.0.8、v0.0.7 |
| 听风 WindTone（Android 本地音乐播放器） | [`WindTone/`](WindTone/) | [v1.2.61](WindTone/v1.2.61/) | v1.2.61、v1.2.60、v1.2.59、v1.2.58、v1.2.57 |

## 下载

每个版本目录下按 CPU 架构分 5 个包：

| 安装包 | 适用设备 |
|---|---|
| `*-arm64-v8a.apk` | 绝大多数手机 / 车机（64 位 ARM） |
| `*-armeabi-v7a.apk` | 较老的 32 位 ARM 设备 |
| `*-x86_64.apk` | 模拟器 / x86 设备 |
| `*-x86.apk` | 老旧 32 位模拟器 |
| `*-universal.apk` | 全架构合一，体积略大；拿不准架构时用它 |

直链格式：

```
https://raw.githubusercontent.com/LuckyLearning/Release/main/<软件>/v<版本>/<文件名>
```

## 校验

每个版本目录下的 `checksums.txt` 是各包的 SHA-256：

```bash
cd <软件>/v<版本> && sha256sum -c checksums.txt
```

## 保留策略

每个软件目录下**只保留最近 5 个版本**（按版本号排序）。发布流水线在写入新版本后会自动删除更旧的目录，
并同步刷新本文件与 `latest.json`。
