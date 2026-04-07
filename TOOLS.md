# TOOLS.md - Local Notes

Skills define _how_ tools work. This file is for _your_ specifics — the stuff that's unique to your setup.

## What Goes Here

Things like:

- Camera names and locations
- SSH hosts and aliases
- Preferred voices for TTS
- Speaker/room names
- Device nicknames
- Anything environment-specific

## Examples

```markdown
### Cameras

- living-room → Main area, 180° wide angle
- front-door → Entrance, motion-triggered

### SSH

- home-server → 192.168.1.100, user: admin

### TTS

- Preferred voice: "Nova" (warm, slightly British)
- Default speaker: Kitchen HomePod
```

## Why Separate?

Skills are shared. Your setup is yours. Keeping them apart means you can update skills without losing your notes, and share skills without leaking your infrastructure.

---

## ETF投资分析工具配置 (继承自 AnalyzeMaster)

### AKShare
- **状态**: ✅ 已安装 (v1.18.39)
- **Python环境**: `/home/ubuntu/.openclaw/workspace-stock_analyzer/venv/bin/python`
- **特点**: 免费、无需注册、数据丰富
- **适用场景**: A股实时/历史行情、基本面数据、宏观经济数据

### Tushare
- **Token**: `8bacc6df4a2e60ce93c5ce1aaddfeb14c854da49eb262861f2f57f07`
- **状态**: ✅ 已配置
- **注册时间**: 2026-03-14
- **特点**: 专业金融数据接口，积分制
- **适用场景**: 财务数据、机构持仓、龙虎榜等专业数据

### QVeris
- **API Key**: `sk-PB-WKEjgzidzu6K2T4SpJV-c3jcHbvkfRUDKKJUHbAg`
- **状态**: ✅ 已配置
- **Skill路径**: `/home/ubuntu/.openclaw/workspace/skills/qveris-official/`
- **功能**: A股ETF历史数据获取（基于同花顺iFinD）
- **数据源**: 同花顺(THS) iFinD专业金融数据库

### ETF Investment Analyzer Skill
- **路径**: `/home/ubuntu/.openclaw/workspace/skills/etf-investment-analyzer/`
- **功能**: 完整的ETF投资分析系统
  - 多时间框架分析（长期1年+短期1月滚动数据）
  - 技术指标计算（MA, MACD, RSI, KDJ, 布林带）
  - 策略回测和优化
  - 自动每日报告生成
  - 飞书文档集成

### 自建ETF分析脚本 (Analyzemaster)
- **路径**: `/home/ubuntu/.openclaw/workspace-rtl_agent/analyzemaster/`
- **核心脚本**:
  - `etf_strategy_backtest.py` - 12种策略回测
  - `etf_monitor.py` - 1456只A股ETF实时监控
  - `etf_backtest_2024.py` - 2024年回测
  - `finclaw_etf_backtest.py` - FinClaw集成回测
- **数据文件**:
  - `etf_list.json` - 1456只ETF列表
  - `backtest_results.json` - 回测结果

### FinClaw AI量化引擎
- **版本**: v5.1.0
- **安装路径**: `/home/ubuntu/.openclaw/workspace/skills/finclaw`
- **Python包**: `finclaw-ai==5.1.0`
- **功能**:
  - 20+内置策略（网格交易、配对交易、趋势跟踪等）
  - AI策略生成（自然语言生成策略）
  - 模拟交易系统
  - MCP服务器（AI Agent集成）

### 使用方式
```bash
# 激活虚拟环境
source /home/ubuntu/.openclaw/workspace-stock_analyzer/venv/bin/activate

# ETF Investment Analyzer
python3 /home/ubuntu/.openclaw/workspace/skills/etf-investment-analyzer/scripts/etf_analyzer.py

# AnalyzeMaster 自建脚本
cd /home/ubuntu/.openclaw/workspace-rtl_agent/analyzemaster
python3 etf_strategy_backtest.py
python3 etf_monitor.py --all

# FinClaw
finclaw backtest --ticker 510050 --strategy golden-cross
finclaw analyze 510050 --indicators rsi,macd,bollinger
```

---

## GitHub API 配置

### GitHub Token
- **状态**: ✅ 已配置
- **路径**: `/home/ubuntu/.openclaw/secrets/github_token.txt`
- **账号**: anekin

---

Add whatever helps you do your job. This is your cheat sheet.
