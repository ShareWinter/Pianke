# 片刻

> 记录每一次观影，决定今晚看什么。

片刻是一款本地优先的私人观影助手。它不是电影社区，也不是云端片库，而是帮你管理自己的影片、记录观影经历，并在选择困难时用抽片流程快速决定下一部要看的作品。

## ✨ Features

- **本地片库**：影片数据保存在本机，适合维护自己的私人片单。
- **多入口添加**：支持影片搜索、豆瓣链接、豆瓣片单链接和手动添加。
- **细化观影记录**：记录观看日期、心情、同伴、评分、短评和重看状态。
- **抽片决策**：支持常规抽取、三选一、筛选后抽取等流程。
- **合集抽片**：从指定合集直接抽片，让“今晚看什么”更贴合场景。
- **观影历史**：列表与日历视图回顾自己的观影节奏。
- **标签与合集**：用标签、手动合集和智能合集整理片库。
- **本地备份**：导出/导入 JSON 备份，不依赖服务器。

## 📱 Screenshots

> Screenshots coming soon.

建议补充以下截图：

- 片库首页
- 添加影片
- 抽片流程
- 三选一结果
- 观影记录
- 合集详情
- 备份设置

## 🧱 Tech Stack

- Flutter
- Provider
- go_router
- sqflite
- SharedPreferences
- Dio
- CachedNetworkImage

## 📂 Project Structure

```text
lib/
  config/       # Theme and app configuration
  models/       # Data models and serialization
  services/     # Storage, scraping, draw logic, backup
  providers/    # ChangeNotifier state management
  pages/        # Route-level screens
  widgets/      # Reusable UI components
  router/       # go_router configuration
```

## 🚀 Getting Started

Install dependencies:

```bash
flutter pub get
```

Run in debug mode:

```bash
flutter run
```

Run on a specific device:

```bash
flutter run -d <device-id>
```

Analyze code:

```bash
flutter analyze
```

Run tests:

```bash
flutter test
```

Build Android APK:

```bash
flutter build apk
```

## 🗃️ Data & Privacy

片刻采用本地优先设计。影片、观影记录、合集、标签和抽片历史默认保存在本机数据库中，不需要账号，也不会上传到服务器。

备份功能会导出明文 JSON 文件，方便你自行保存、迁移或检查数据。请妥善保管备份文件。

## 🎬 About Movie Metadata

片刻可以从豆瓣页面导入影片资料和海报，但豆瓣只是资料来源之一。应用核心仍然是私人片库、观影记录和抽片决策。

## 🛠️ Development Notes

- 使用 `AppTheme` 中的颜色、间距和圆角 token。
- 页面层不要直接访问数据库或网络，优先通过 Provider/Service。
- 数据结构变更需要考虑 SQLite 迁移和备份兼容。
- 新增测试文件请放在 `test/`，文件名以 `_test.dart` 结尾。

## 📦 Backup Compatibility

当前备份标识为 `Pianke`，并兼容旧版本 `RandoMov` 备份文件。

## License

No license has been specified yet.
