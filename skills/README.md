# Skills 目录备份清单

本目录包含已安装的 OpenClaw Skills，用于快速恢复环境。

## 已安装 Skills (25个)

### 📊 股票分析 (11个)
| Skill | 来源 | 功能 |
|-------|------|------|
| **finclaw** | 本地 | AI量化引擎，20+内置策略，回测、模拟交易 |
| **etf-backtest** | 本地 | ETF回测分析 |
| **etf-trading-backtest** | 本地 | ETF交易策略回测 |
| **akshare-stock** | 本地 | A股数据获取（AKShare） |
| **new-akshare-stock** | 本地 | 新版AKShare股票数据 |
| **china-stock-analysis** | 本地 | 中国股市分析 |
| **a-stock-market** | 本地 | A股市场数据 |
| **a-stock-trading-assistant** | 本地 | A股交易助手 |
| **ftshare-etf-data** | 本地 | ETF数据获取 |
| **openclaw-stock-monitor** | 本地 | 股票监控提醒 |
| **tradingview-strats** | 本地 | TradingView策略 |

### 🔍 搜索与信息 (5个)
| Skill | 来源 | 功能 |
|-------|------|------|
| **web_search** | 内置 | 网页搜索 |
| **web_fetch** | 内置 | 网页内容获取 |
| **multi-search-engine** | clawhub | 17个搜索引擎集成 |
| **openclaw-tavily-search** | clawhub | Tavily API搜索 |
| **arxiv-search-collector** | clawhub | arXiv论文搜索 |
| **news-aggregator** | clawhub | 新闻聚合 |
| **qveris-official** | clawhub | 同花顺iFinD数据 |
| **find-skills-skill** | clawhub | 技能搜索发现 |

### 🤖 系统与自动化 (7个)
| Skill | 来源 | 功能 |
|-------|------|------|
| **feishu-doc** | 内置 | 飞书文档操作 |
| **feishu-wiki** | 内置 | 飞书知识库 |
| **feishu-drive** | 内置 | 飞书云存储 |
| **feishu-bitable** | 内置 | 飞书多维表格 |
| **ke-office-automation** | clawhub | Excel/Word批量处理 |
| **github-ops** | clawhub | GitHub操作 |
| **notion** | clawhub | Notion集成 |
| **obsidian** | clawhub | Obsidian集成 |
| **session-logs** | clawhub | 会话日志管理 |

### 🧠 AI与语音 (3个)
| Skill | 来源 | 功能 |
|-------|------|------|
| **openai-whisper-api** | clawhub | 语音识别 |
| **summarize** | clawhub | 文本摘要 |
| **agent-team-orchestration** | clawhub | 多Agent协作 |

## 核心技能说明

### finclaw - AI量化引擎
- 20+内置交易策略
- 支持A股、美股、加密货币
- 策略回测和优化
- 模拟交易系统
- AI策略生成（自然语言）

### 股票分析技能组
- AKShare数据源（免费）
- Tushare数据源（专业）
- QVeris/同花顺iFinD（机构级）
- 技术指标计算（MA、MACD、RSI、KDJ、布林带）
- ETF监控和提醒

### 飞书集成技能组
- 文档读写操作
- 知识库管理
- 云文件管理
- 多维表格操作

## 恢复方法

### 从 ClawHub 安装
```bash
# 搜索技能
npx clawhub search <keyword>

# 安装技能
npx clawhub install <skill-name> --force
```

### 本地 Skills
本地开发的 skills 需要从源码恢复：
- 从备份目录复制到 `~/.openclaw/workspace/skills/`

### 配置 API Keys
部分技能需要配置 API Key：
- `qveris-official`: QVERIS_API_KEY
- `tushare`: TUSHARE_TOKEN
- `finclaw`: 无需配置（本地运行）

## 注意事项
1. 部分 skills 需要额外配置（如 API Key）
2. 安装后检查 SKILL.md 了解具体使用方法
3. 某些 skills 可能有系统依赖（如 FFmpeg）

---
**最后更新**: 2026-04-07
**技能总数**: 25个
**备份目的**: 数字分身复活时使用
