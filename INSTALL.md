# Renaissance Team 安装指南

本指南将帮助你安装和配置 Renaissance（复兴计划）团队。

## 📋 安装前准备

### 系统要求
- Claude Code CLI 已安装
- 对应的 MCP 服务器已配置（如需要）
- 适当的文件系统权限

### MCP 服务器依赖

本团队的某些专家成员使用 MCP 工具，需要预先配置以下 MCP 服务器：

| MCP 服务器 | 用途 | 使用成员 |
|-----------|------|----------|
| sequential-thinking | 深度思考推理 | Decoder, Pathfinder, Bridge, Palette |
| context7 | 技术文档查询 | Decoder, Pathfinder, Bridge, Mimic, Palette |

> ⚠️ **注意**：如果未配置这些 MCP 服务器，相关专家将使用基础工具完成任务。

## 🚀 安装步骤

### 步骤 1: 复制团队文件

将整个 `renaissance-team` 目录复制到你的技能目录：

**Windows**:
```bash
# 默认技能目录
C:\Users\[YourUsername]\.claude\skills\renaissance-team\
```

**macOS/Linux**:
```bash
# 默认技能目录
~/.claude/skills/renaissance-team/
```

### 步骤 2: 验证文件结构

确保以下文件结构正确：

```
        └── skill.md                   # ✅ 必需
```

### 步骤 3: 重启 Claude Code

安装完成后，重启 Claude Code 以加载新技能。

## ✅ 验证安装

### 测试命令

在 Claude Code 中运行：

```
/renaissance-coordinator 帮我分析这个项目的迁移可行性
```

如果协调器正确响应并开始任务规划，说明安装成功。

### 检查清单

- [ ] 协调器技能可以正常触发
- [ ] 所有专家代理可以被正确调用
- [ ] MCP 工具授权机制正常工作（如配置了 MCP）
- [ ] 混合型执行模式可以正确切换

## 🔧 配置选项

### 禁用 MCP 工具

如果不想使用 MCP 工具，可以在触发协调器时选择拒绝授权：

```
用户: /renaissance-coordinator 分析代码逻辑
协调器: 预估需要使用 MCP 工具，是否同意？
用户: 拒绝使用，全部用基础工具完成
```

### 自定义工作目录

协调器默认使用 `{项目}/.renaissance/` 作为工作目录。如需自定义，在触发时指定：

```
/renaissance-coordinator 分析项目，工作目录使用 custom/.work/
```

## 📚 使用指南

### 基本用法

```
/renaissance-coordinator [任务描述]
```

### 高级用法

**指定执行模式**:
```
/renaissance-coordinator 使用混合模式分析项目
/renaissance-coordinator 只进行资产分析（并行模式）
```

**指定 MCP 授权**:
```
/renaissance-coordinator 分析代码，同意使用必要的 MCP 工具
```

## 🐛 故障排查

### 问题 1: 协调器无法触发

**症状**: 运行 `/renaissance-coordinator` 没有响应

**解决方案**:
1. 检查文件路径是否正确
2. 确认 `skill.md` 中的 description 格式正确
3. 重启 Claude Code

### 问题 2: 专家代理无法调用

**症状**: 协调器报告无法找到专家代理

**解决方案**:
1. 检查 `agents/` 目录中的文件名格式
2. 确认每个 agent 的 `name` 字段正确
3. 验证 description 使用双引号包裹

### 问题 3: MCP 工具无法使用

**症状**: 专家报告 MCP 工具不可用

**解决方案**:
1. 确认 MCP 服务器已正确配置
2. 检查 agent 的 tools 字段是否包含 MCP 工具
3. 确认协调器已授权 MCP 工具使用

### 问题 4: 产出文件路径错误

**症状**: 专家报告无法找到指定路径

**解决方案**:
1. 检查协调器触发指令中的路径格式
2. 确认使用 `{项目}/.renaissance/` 格式
3. 验证工作目录是否存在

## 📞 获取帮助

如遇到其他问题：

1. 查看 [README.md](./README.md) 了解团队详情
2. 检查各个专家的 agent.md 文件了解具体配置
3. 查看协调器的 skill.md 了解工作流程

## 🔄 卸载

如需卸载 Renaissance Team：

1. 删除技能目录：
   ```bash
   # Windows
   rmdir /s "C:\Users\[YourUsername]\.claude\skills\renaissance-team"

   # macOS/Linux
   rm -rf ~/.claude/skills/renaissance-team
   ```

2. 重启 Claude Code

## 📝 更新记录

### v3.0 (2026-03-01)
- 升级到 super-team-builder v3.0 模板
- 新增三级 MCP 授权机制
- 优化通信协议和触发格式
- 完善故障排查指南
