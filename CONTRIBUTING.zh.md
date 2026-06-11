# 贡献指南

感谢您对 minimax-usage 项目所给予的关注与支持。本文档系统地介绍了从搭建开发环境到提交 Pull Request 的完整流程。请在开始工作之前完整阅读本文档，以确保您的贡献能够顺利通过审核与合并。

## 关于本项目

minimax-usage 是一个 Claude Code 插件，用于在 Claude Code 的 HUD 状态栏中展示 MiniMax 套餐的剩余使用情况。本项目采用 TypeScript 进行开发，最终构建产物为可在 Node.js 18+ 环境中运行的 JavaScript 文件。

## 行为准则

参与本项目的所有互动均应保持专业与包容的态度。期待每一位贡献者：

- 使用友好、包容的语言
- 尊重不同的观点与经验
- 诚恳地接受建设性意见
- 以对项目最有利的方式行事

如遇任何不当行为，请联系项目维护者。

## 提交 Issue

在提交 Issue 之前，请先检索现有 Issue 列表，确认问题未被重复提出。本仓库提供以下两类 Issue 模板：

- **Bug Report**：用于反馈项目运行中出现的异常
- **Feature Request**：用于提出新功能或改进建议

请按照对应模板的要求尽可能完整地填写信息，以便维护者能够快速定位与处理。

## 开发环境

### 必要依赖

- Node.js 18 或更高版本
- npm 9 或更高版本
- 支持 Claude Code 的运行环境（用于本地调试）

### 拉取代码与安装

```bash
git clone https://github.com/PureLo/minimax-usage.git
cd minimax-usage
npm install
```

### 本地构建

```bash
npm run build
```

### 持续构建

```bash
npm run dev
```

该命令以 watch 模式启动 TypeScript 编译器，便于在修改源代码后即时查看结果。

## 代码规范

- 严格遵循现有代码风格与目录结构
- 公共函数与导出的类型需添加 TSDoc 注释
- 提交前请确认 `npm run build` 能够通过，且无新增 TypeScript 错误
- 避免引入非必要的运行时依赖；如确有必要，请在 PR 描述中详细说明理由
- 保持提交粒度清晰，一次 Pull Request 仅解决一个问题

## 提交信息规范

本项目遵循 [Conventional Commits](https://www.conventionalcommits.org/zh-hans/) 规范。提交信息格式如下：

```
<类型>(<可选范围>): <简短说明>

<可选正文>

<可选脚注>
```

常用类型如下：

| 类型 | 用途 |
| --- | --- |
| feat | 新增功能 |
| fix | 修复缺陷 |
| docs | 文档变更 |
| style | 不影响代码含义的格式调整 |
| refactor | 既非新增功能也非修复缺陷的代码重构 |
| test | 新增或修改测试 |
| chore | 构建流程、辅助工具或依赖项变更 |

## Pull Request 流程

1. Fork 本仓库，并基于 `main` 分支创建特性分支。建议采用 `feat/xxx`、`fix/xxx` 或 `docs/xxx` 等形式命名
2. 提交变更时遵循上述提交信息规范
3. 提交 Pull Request 之前，请确认本地 `npm run build` 仍然通过
4. 推送至您 Fork 的仓库，并向上游 `PureLo/minimax-usage` 的 `main` 分支发起 Pull Request
5. **务必在 Pull Request 描述中附上修改前后的对比截图**。本插件的核心交付物是状态栏的最终展示效果，截图是审阅者评估变更最直接、最可靠的依据
6. 在 CI 通过、CodeRabbit 审核意见已被处理、并获得至少一位维护者批准后，Pull Request 将被合并

### 截图要求

本插件运行于终端环境中，截图时请使用系统截图工具捕获 Claude Code 状态栏所在的终端区域。Pull Request 描述中应包含以下内容：

- **修改前**：复现原始状态或问题的截图
- **修改后**：应用本次变更后的截图
- 简要说明两张截图之间的差异，必要时附上对应的文本输出

若本次变更仅涉及非可视化逻辑（如配置解析、缓存策略、错误处理等），可在 Pull Request 描述中明确说明该情况，并附上相应的测试输出或日志作为佐证。仅包含文档修订、`chore` 类变更的 Pull Request，可以不提供截图。

## 版本与发布

本项目版本号遵循 [语义化版本](https://semver.org/lang/zh-CN/) 规范。版本号的更新与发布由维护者手动完成，贡献者无需自行修改 `package.json` 中的 `version` 字段。

## 许可协议

向本项目提交的贡献，将依据 MIT 协议进行许可。

## 联系方式

如有疑问，可在相关 Issue 或 Pull Request 中留言，或通过项目主页所列的联系方式与维护者取得联系。
