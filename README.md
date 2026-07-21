# 蛰龙令 - 龙头狙击交易终端

## 一键构建APK

### 方法1：GitHub Actions自动构建（推荐）

1. **Fork本仓库**到你的GitHub账号
2. 进入仓库 → Actions → 点击"Build Android APK" → "Run workflow"
3. 等待约5分钟构建完成
4. 进入Releases页面，下载APK文件
5. 手机安装即可使用

### 方法2：本地编译

需要：Node.js 18+、Android Studio、Java 17

```bash
# 1. 安装依赖
npm install

# 2. 添加Android平台
npx cap add android

# 3. 同步Web资源
npx cap sync android

# 4. 打开Android Studio
npx cap open android

# 5. 在Android Studio中点击"Build → Build Bundle(s) / APK(s) → Build APK(s)"
```

### 方法3：直接安装PWA

如果不需要APK，可以直接用手机浏览器打开 `index.html`，添加到主屏幕即可。

## 功能特性

- ✅ 实时连接A股数据（腾讯财经API）
- ✅ 大盘20日均线监控
- ✅ 热点板块扫描（S级/A级判定）
- ✅ 持仓管理（止盈止损线实时显示）
- ✅ 交易日志（本地永久保存）
- ✅ 离线可用（无网络也能查看持仓）
- ✅ 全屏运行，无浏览器UI

## 策略参数

| 参数 | 默认值 |
|------|--------|
| 初始资金 | ¥200,000 |
| 硬止损 | -3% |
| 动态止盈 | 最高价回落5% |
| 最长持仓 | 8天 |
| S级仓位 | 20% |
| A级仓位 | 15% |
| 最大持仓 | 2只 |

## 数据来源

- 上证指数实时数据：腾讯财经API
- 20日均线计算：腾讯K线API
- 持仓股价更新：腾讯实时行情API

## 免责声明

本APP仅供学习研究使用，不构成投资建议。股市有风险，投资需谨慎。
