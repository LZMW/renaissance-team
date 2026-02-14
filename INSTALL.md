# Renaissance（复兴计划）- 安装指南

## 前置条件

- Claude Code CLI 已安装
- 配置目录: `~/.claude/` (Windows: `C:\Users\[用户名]\.claude\`)

## 自动安装（已完成）

团队配置文件已自动安装到以下位置：

```
C:\Users\29493\.claude\
├── agents\
│   ├── renaissance-decoder.md      ✅ 已安装
│   ├── renaissance-pathfinder.md   ✅ 已安装
│   ├── renaissance-bridge.md       ✅ 已安装
│   ├── renaissance-mimic.md        ✅ 已安装
│   ├── renaissance-palette.md      ✅ 已安装
│   └── renaissance-vault.md        ✅ 已安装
└── skills\
    └── renaissance-coordinator\
        └── skill.md                ✅ 已安装
```

## 手动安装（如需在其他机器安装）

### 步骤1: 复制 Agents

```bash
# Windows (Git Bash)
cp -r renaissance-team/agents/*.md ~/.claude/agents/

# macOS / Linux
cp -r renaissance-team/agents/*.md ~/.claude/agents/
```

### 步骤2: 复制 Skills

```bash
# Windows (Git Bash)
cp -r renaissance-team/skills/renaissance-coordinator ~/.claude/skills/

# macOS / Linux
cp -r renaissance-team/skills/renaissance-coordinator ~/.claude/skills/
```

### 步骤3: 重启 Claude Code

```bash
# 重启 Claude Code CLI
claude
```

## 验证安装

### 方法1: 检查文件存在

```bash
# 检查 agents
ls ~/.claude/agents/renaissance-*.md

# 检查 skills
ls ~/.claude/skills/renaissance-coordinator/skill.md
```

### 方法2: 测试触发

在 Claude Code 中输入以下命令测试：

```
# 测试协调器
使用 renaissance-coordinator 来帮我分析一个旧项目的迁移需求

# 测试专家
使用 renaissance-decoder 来分析这段旧代码
使用 renaissance-vault 来扫描我的项目目录
```

## 触发关键词速查

### 协调器触发词
- "项目迁移"、"旧项目"、"代码迁移"
- "资产现代化"、"引擎升级"、"平台迁移"

### Decoder 触发词
- "代码分析"、"逆向"、"逻辑提取"
- "旧代码理解"、"算法还原"

### Pathfinder 触发词
- "迁移策略"、"迁移规划"、"技术选型"
- "升级路线"、"风险评估"

### Bridge 触发词
- "资源加载"、"转换脚本"、"格式转换"
- "资源管线"、"兼容层"

### Mimic 触发词
- "代码重写"、"复刻"、"现代化"
- "功能实现"、"代码移植"

### Palette 触发词
- "资产优化"、"贴图压缩"、"模型优化"
- "着色器"、"纹理"、"格式"

### Vault 触发词
- "资产盘点"、"目录扫描"、"去重"
- "命名规范"、"文件整理"

## 卸载

如需卸载，删除以下文件：

```bash
# 删除 agents
rm ~/.claude/agents/renaissance-*.md

# 删除 skills
rm -rf ~/.claude/skills/renaissance-coordinator
```

## 故障排除

### Q: 触发关键词不生效？
A: 确保文件已正确放置在配置目录，并重启 Claude Code。

### Q: 专家没有按预期响应？
A: 检查 agent 文件的 YAML frontmatter 格式是否正确。

### Q: 协调器没有触发专家？
A: 协调器需要明确的任务描述，尝试使用更具体的触发词。

## 版本信息

- 团队名称: Renaissance（复兴计划）
- 版本: 1.0.0
- 创建日期: 2026-02-14
- 专家数量: 6位
