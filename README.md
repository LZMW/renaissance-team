# Renaissance（复兴计划）- 遗产项目迁移专家团队

## 概述

**Renaissance（复兴计划）** 是一个跨领域特种小组，负责将**陈旧项目（代码逻辑与美术资产）** 移植到现代引擎或平台。实现**代码与资产的双重现代化**。

## 团队类型

**混合型团队** - 根据任务特点智能选择串行/并行/混合执行模式

## 🚀 快速开始

### 最佳实践：使用斜杠命令触发

```
/renaissance-coordinator [你的任务描述]
```

**示例：**
```
/renaissance-coordinator 帮我把这个 Unity 4 项目迁移到 Unity 2023
/renaissance-coordinator 扫描项目目录，找出所有冗余资产
/renaissance-coordinator 这段旧代码需要用 TypeScript 重写
/renaissance-coordinator 评估从 WebGL 1.0 迁移到 WebGPU 的方案
```

> 💡 **提示**：使用 `/renaissance-coordinator` 是最推荐的触发方式，协调器会自动分析任务并分配合适的专家。

## 层级架构

```
Renaissance Coordinator（协调器）
├── 逻辑攻坚组（串行流程）
│   ├── Decoder（逆向分析师）- 代码考古、逻辑提取
│   ├── Pathfinder（战略规划师）- 迁移策略、技术选型
│   ├── Bridge（跨栈架构师）- 架构设计、资源管线
│   └── Mimic（复刻专家）- 代码复刻、现代化改造
└── 资产攻坚组（并行流程）
    ├── Palette（美术考古家）- 贴图压缩、模型优化
    └── Vault（资产审计官）- 目录扫描、去重分析
```

## 团队成员

| 代号 | 角色 | 核心能力 | 触发关键词 |
|------|------|----------|------------|
| Decoder | 逆向分析师 | 代码考古、逻辑提取、算法还原 | 代码分析、逆向、逻辑提取 |
| Pathfinder | 战略规划师 | 迁移策略、技术选型、路线规划 | 迁移规划、策略、技术选型 |
| Bridge | 跨栈架构师 | 架构设计、转换脚本、资源管线 | 架构设计、转换脚本、管线 |
| Mimic | 复刻专家 | 代码复刻、现代化、功能实现 | 代码重写、复刻、现代化 |
| Palette | 美术考古家 | 贴图压缩、模型优化、着色器修复 | 资产优化、贴图、模型、着色器 |
| Vault | 资产审计官 | 目录扫描、去重、命名规范 | 资产盘点、去重、命名规范 |

## 执行模式

### 混合型工作流程

协调器根据任务特点智能选择执行模式：

**全栈迁移模式**（混合）:
```
1. [Decoder] 代码逆向 → 产出分析
2. [Vault & Palette] 并行资产分析
3. [Pathfinder] 基于分析制定策略
4. [Bridge] 设计架构和资源管线
5. [Mimic] 复刻现代化代码
```

**代码迁移模式**（串行）:
```
Decoder → Pathfinder → Bridge → Mimic
```

**资产清理模式**（并行）:
```
Vault ∥ Palette
```

## 典型使用场景

### 场景1: 游戏引擎升级
```
用户: /renaissance-coordinator 我们要从 Unity 4 升级到 Unity 2023

→ 协调器分析 → 启动混合模式
→ 逻辑线: Decoder → Pathfinder → Bridge → Mimic
→ 资产线: Vault ∥ Palette
→ 汇总: 完整迁移方案
```

### 场景2: 平台迁移
```
用户: /renaissance-coordinator 我们的 Flash 游戏要迁移到 HTML5

→ 协调器分析 → 启动混合模式
→ 输出: 代码重构方案 + 资产优化方案 + 迁移检查表
```

### 场景3: 资产清理
```
用户: /renaissance-coordinator 项目积累了10年的垃圾文件，帮我清理

→ Vault 扫描目录 → 识别冗余 → 生成清理报告
```

## 交付物清单

| 交付物 | 负责人 | 说明 |
|--------|--------|------|
| 代码逆向分析报告 | Decoder | 逻辑痛点、算法规则、依赖关系 |
| 迁移战略规划书 | Pathfinder | 技术选型、分阶段计划、风险矩阵 |
| 资源加载管理器 | Bridge | 通用资源加载/卸载代码模块 |
| 格式转换脚本 | Bridge | 批量格式转换工具 |
| 资产优化分析报告 | Palette | 贴图、模型、着色器优化建议 |
| 资产迁移与盘点表 | Vault | 完整资产清单、状态追踪 |
| 项目结构重构树 | 协调器 | 推荐的新目录结构 |

## 专家座右铭

| 专家 | 座右铭 |
|------|--------|
| Decoder | "每一行被遗忘的代码都有它存在的理由。我是代码考古学家。" |
| Pathfinder | "没有地图的迁移是灾难的开始。我负责绘制通往未来的路线。" |
| Bridge | "代码与资产之间的桥梁。没有我，新代码找不到新资源。" |
| Mimic | "理解原作的灵魂，用现代的语言重新演绎。形似更要神似。" |
| Palette | "每一张 4K 贴图如果只显示在一个 50px 的 UI 图标上，都是对显存的犯罪。" |
| Vault | "混乱的目录结构是项目崩溃的开始。我知道每一个文件该去哪里。" |

## 安装方法

详见 [INSTALL.md](./INSTALL.md)

## 文件清单

```
renaissance-team/
├── README.md                          # 团队说明
├── INSTALL.md                         # 安装指南
├── agents/
│   ├── renaissance-decoder.md         # 逆向分析师
│   ├── renaissance-pathfinder.md      # 战略规划师
│   ├── renaissance-bridge.md          # 跨栈架构师
│   ├── renaissance-mimic.md           # 复刻专家
│   ├── renaissance-palette.md         # 美术考古家
│   └── renaissance-vault.md           # 资产审计官
└── skills/
    └── renaissance-coordinator/
        └── skill.md                   # 协调器
```

## License

MIT

---

## 更新日志

### 2026-03-01 (v3.0)
- 🎉 升级到 super-team-builder v3.0 新模板
- ✅ 优化协调器和专家代理配置
- 📚 完善安装指南和使用文档
- 🔧 统一通信协议（📂📋🔓 标准格式）
- 🔐 嵌入三级MCP授权机制
