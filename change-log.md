# 正式版本更新日志

历史 beta 版本更新记录见 [BETA版本更新日志](beta-change-log.md)。

## v2.3.1

发布时间 2026/10/23

### 升级版本

逐步执行以下命令，最后清除**浏览器缓存**
```bash
composer require gzxy/dcat-admin:"2.3.1"
php artisan admin:update # 不会覆盖翻译文件 menu.php 以及 global.php
```

### 修复

1. 页脚 `Powered by` 链接指向本仓库（[gzxy0102/dcat-admin](https://github.com/gzxy0102/dcat-admin)）

## v2.3.0

发布时间 2026/10/23

`gzxy/dcat-admin` 的首个正式版本。本包是 [jqhph/dcat-admin](https://github.com/jqhph/dcat-admin)（原 `dcat/laravel-admin`）的维护分支，包内命名空间（`Dcat\Admin`）与配置完全不变。

### 升级版本

从 `dcat/laravel-admin` 迁移：
```bash
composer remove dcat/laravel-admin
composer require gzxy/dcat-admin:"2.3.0"
php artisan admin:update
```

### 新增功能

1. **支持 Laravel 13**（整体兼容范围 Laravel 5.5 ~ 13.x，PHP >= 7.1）
2. 包名迁移为 `gzxy/dcat-admin`，并通过 `replace` 声明兼容依赖 `dcat/laravel-admin` 的扩展，生态扩展无需修改即可继续使用

### 修复

1. `spatie/eloquent-sortable` 依赖支持 5.x（Laravel 13 所需）

### 其他

1. CI 补全 Laravel 5.5 ~ 13 全版本测试矩阵（Feature + Dusk 浏览器测试，共 18 个 job）
