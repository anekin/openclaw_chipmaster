# HEARTBEAT.md

# ETF投资分析定时任务

## 每日监控清单

### 早盘前 (8:00-8:30)
- [ ] 运行数据收集脚本
- [ ] 生成每日分析报告
- [ ] 同步到飞书文档

### 盘中监控 (9:30-15:00)
- [ ] ETF涨跌幅超过±3%提醒
- [ ] 持仓ETF技术信号检查

### 收盘后 (15:00-16:00)
- [ ] 更新持仓数据
- [ ] 记录交易日志
- [ ] 备份分析数据

## 使用方法

```bash
# 每日数据收集
python3 /home/ubuntu/.openclaw/workspace/skills/etf-investment-analyzer/scripts/daily_data_collection.py

# 生成报告
python3 /home/ubuntu/.openclaw/workspace/skills/etf-investment-analyzer/scripts/daily_report.py

# ETF监控
python3 /home/ubuntu/.openclaw/workspace-rtl_agent/analyzemaster/etf_monitor.py --all
```

## 自动化建议

```bash
# 编辑 crontab
crontab -e

# 添加以下任务
# 每日8:00运行数据收集
0 8 * * 1-5 cd /home/ubuntu/.openclaw/workspace-rtl_agent && python3 analyzemaster/etf_monitor.py --all >> /tmp/etf_monitor.log 2>&1

# 每30分钟监控一次（交易日）
*/30 9-15 * * 1-5 cd /home/ubuntu/.openclaw/workspace-rtl_agent && python3 analyzemaster/etf_monitor.py >> /tmp/etf_monitor.log 2>&1
```
