# Roco AI Battle Assistant - 洛克王国AI战斗助手

一个基于计算机视觉和人工智能的洛克王国战斗自动检测与决策系统。

## 项目简介

本项目旨在通过计算机视觉技术自动识别洛克王国游戏中的战斗场景，并利用人工智能算法进行战斗决策规划，实现自动化战斗操作。

### 核心功能

- 👁️ **视觉识别** - 自动检测游戏画面中的战斗场景、精灵状态、技能信息
- 🧠 **智能决策** - 基于当前战斗状态，AI自动规划最优战斗策略
- 🎮 **自动操作** - 根据决策结果自动执行技能选择、道具使用等操作
- 📊 **战斗分析** - 记录战斗数据，提供战斗效率分析

## 技术架构

### 视觉识别模块
- **屏幕捕获** - 实时获取游戏画面
- **图像处理** - OpenCV进行图像预处理和特征提取
- **目标检测** - 识别战斗界面元素（血条、技能按钮、精灵状态）
- **OCR识别** - 识别战斗中的文字信息（技能名称、伤害数值）

### AI决策模块
- **状态评估** - 分析当前战斗双方的状态
- **策略生成** - 基于规则或强化学习生成战斗策略
- **决策执行** - 选择最优行动方案

### 自动操作模块
- **模拟输入** - 模拟鼠标点击、键盘操作
- **操作验证** - 验证操作是否成功执行

## 技术栈

- **Python 3.10+** - 主要开发语言
- **OpenCV** - 计算机视觉处理
- **PyTorch / TensorFlow** - 深度学习框架（可选）
- **PyAutoGUI / pynput** - 自动化操作
- **Tesseract OCR** - 文字识别
- **SQLite** - 数据存储

## 快速开始

### 环境准备

```bash
# 克隆项目
git clone https://github.com/your-username/roco-ai-battle-assistant.git
cd roco-ai-battle-assistant

# 创建虚拟环境
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# 安装依赖
pip install -r requirements.txt

# 安装Tesseract OCR（Windows需要额外安装）
# 下载地址: https://github.com/UB-Mannheim/tesseract/wiki
```

### 运行程序

```bash
# 启动主程序
python main.py

# 或使用图形界面
python gui.py
```

## 项目结构

```
roco-ai-battle-assistant/
├── main.py                    # 程序入口
├── gui.py                     # 图形界面
├── config/
│   ├── settings.py            # 配置文件
│   └── templates/             # 界面模板
├── vision/
│   ├── capture.py             # 屏幕捕获
│   ├── detection.py           # 目标检测
│   ├── recognition.py         # 图像识别
│   └── ocr.py                 # 文字识别
├── ai/
│   ├── state.py               # 状态评估
│   ├── decision.py            # 决策引擎
│   ├── strategy.py            # 策略生成
│   └── models/                # AI模型
├── controller/
│   ├── input.py               # 输入模拟
│   └── executor.py            # 操作执行
├── data/
│   ├── battle_logs/           # 战斗日志
│   ├── templates/             # 图像模板
│   └── database.db            # 数据存储
├── utils/
│   ├── logger.py              # 日志工具
│   └── helpers.py             # 辅助函数
├── tests/                     # 测试文件
├── requirements.txt           # 依赖列表
├── README.md                  # 项目说明
└── LICENSE                    # 许可证
```

## 使用说明

### 基本使用流程

1. **启动程序** - 运行主程序或图形界面
2. **配置参数** - 设置游戏窗口位置、识别参数等
3. **开始监控** - 程序自动监控游戏画面
4. **自动战斗** - 检测到战斗场景后自动进行决策和操作
5. **查看日志** - 战斗结束后查看战斗记录和分析

### 配置说明

主要配置项位于 `config/settings.py`：

- `GAME_WINDOW_TITLE` - 游戏窗口标题
- `DETECTION_INTERVAL` - 检测间隔（毫秒）
- `CONFIDENCE_THRESHOLD` - 识别置信度阈值
- `AUTO_BATTLE_ENABLED` - 是否启用自动战斗

## 开发计划

### 阶段 1：基础框架
- [x] 项目结构搭建
- [ ] 屏幕捕获模块
- [ ] 基础图像处理
- [ ] 图形界面原型

### 阶段 2：视觉识别
- [ ] 战斗场景检测
- [ ] 精灵状态识别
- [ ] 技能按钮识别
- [ ] OCR文字识别

### 阶段 3：AI决策
- [ ] 规则基础决策引擎
- [ ] 状态评估系统
- [ ] 策略库建立
- [ ] 强化学习模型（可选）

### 阶段 4：自动操作
- [ ] 输入模拟模块
- [ ] 操作验证机制
- [ ] 错误处理机制

### 阶段 5：优化完善
- [ ] 性能优化
- [ ] 界面美化
- [ ] 文档完善
- [ ] 正式发布

## 注意事项

### 法律与道德
- 本项目仅供学习研究使用
- 请勿用于商业用途或破坏游戏平衡
- 遵守游戏用户协议和相关法律法规
- 使用本工具产生的一切后果由用户自行承担

### 技术风险
- 游戏更新可能导致识别失效
- 不同分辨率可能需要调整参数
- 建议在测试环境中充分验证后使用

## 免责声明

- 本项目与《洛克王国》官方无关
- 项目开发者不对使用本工具产生的任何后果负责
- 请合理使用，不要滥用自动化工具
- 禁止用于恶意刷取游戏资源或破坏游戏体验

## 许可证

本项目采用 [MIT License](LICENSE) 许可证。

## 贡献指南

欢迎提交 Issue 和 Pull Request 来改进项目！

1. Fork 本仓库
2. 创建你的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交你的更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 提交 Pull Request

## 联系方式

如有问题或建议，欢迎通过以下方式联系：

- 提交 Issue: [GitHub Issues](https://github.com/your-username/roco-ai-battle-assistant/issues)

---

**智能战斗，解放双手！** 🎮🤖

**⚠️ 重要提示：本项目仅供学习交流，请勿用于违反游戏规则的用途。**
