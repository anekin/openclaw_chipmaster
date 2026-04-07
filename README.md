# ChipMaster - OpenClaw Agent Digital Twin

**CodingMaster + AnalyzeMaster** - IC设计与ETF投资分析双料AI助手

---

## 🎯 核心能力

### IC设计 (CodingMaster)
- RTL代码 (Verilog/SystemVerilog)
- Python开发
- 代码架构设计
- 自动化脚本

### ETF投资分析 (AnalyzeMaster)
- 1456只A股ETF实时监控
- 12种经典交易策略回测
- 技术指标：MA、MACD、RSI、KDJ、布林带
- FinClaw AI量化引擎

---

## 📁 核心文件

| 文件 | 说明 |
|------|------|
| `SOUL.md` | 数字分身核心身份定义 |
| `AGENTS.md` | 工作空间管理规范 |
| `IDENTITY.md` | 身份信息 |
| `USER.md` | 用户信息 |
| `TOOLS.md` | 工具配置 |
| `HEARTBEAT.md` | 定时任务配置 |
| `MEMORY.md` | 长期记忆 |
| `memory/` | 每日记忆文件 |
| `scripts/` | 核心脚本链接 |

---

## 🚀 快速开始

### ETF分析
```bash
# ETF策略回测
python3 scripts/etf_strategy_backtest.py

# ETF实时监控
python3 scripts/etf_monitor.py --all

# FinClaw分析
finclaw backtest --ticker 510050 --strategy golden-cross
```

---

## 📝 更新记录

- **2026-04-07**: 初始创建，合并CodingMaster与AnalyzeMaster能力

---

*Created by OpenClaw Agent* 💻📊
