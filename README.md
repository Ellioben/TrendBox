# TrendRadar 热点监控系统

一个基于本项目参考`https://github.com/joyce677/TrendRadar`项目进行简化改造。

## 📁 项目结构

```
Trendbox/
├── core/                          # 核心模块
│   ├── __init__.py
│   ├── data_fetcher.py           # 数据抓取模块
│   ├── data_analyzer.py          # 数据分析模块
│   └── notification_sender.py    # 通知发送模块
├── config/                        # 配置文件
│   ├── __init__.py
│   ├── config_manager.py         # 配置管理模块
│   ├── simple_config.yaml        # 主配置文件
│   └── simple_frequency_words.txt # 关键词配置文件
├── record/                        # 记录文件
│   └── notification_state.json   # 状态记录文件（自动生成）
├── trend_radar.py                # 主程序入口
├── rss-fatch.py                  # RSS抓取工具（独立工具）
├── README.md                     # 项目说明
└── USAGE.md                      # 详细使用说明
```

### 文件说明
- **`trend_radar.py`** - 主程序入口，协调各个模块工作
- **`core/`** - 核心模块文件夹，包含所有业务逻辑
- **`config/`** - 配置文件文件夹，包含配置管理和所有配置
- **`record/`** - 记录文件文件夹，存储运行时状态
- **`rss-fatch.py`** - RSS抓取工具（独立工具）

## 🚀 快速开始

1. **安装依赖**
   ```bash
   pip install requests pyyaml pytz
   ```

2. **配置关键词**
   编辑 `simple_frequency_words.txt` 文件，设置监控的关键词

3. **配置通知**
   编辑 `simple_config.yaml` 文件，设置webhook地址

4. **运行程序**
   ```bash
   python main.py
   ```

## ✨ 主要功能

- **多平台监控**：支持多个个主流新闻平台
- **智能过滤**：基于关键词的智能新闻过滤
- **增量推送**：只推送新增的热点新闻
- **多平台通知**：支持飞书、企业微信、钉钉、Telegram
- **模块化架构**：代码结构清晰，易于维护和扩展

## 📖 详细说明
更多使用说明请查看 [USAGE.md](USAGE.md) 文件。


