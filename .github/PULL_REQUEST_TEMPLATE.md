## 变更说明 / What does this PR do

<!-- 请用 1-3 句话简明扼要地描述本次变更。 -->
<!-- Please summarize this change in 1-3 sentences. -->

## 关联 Issue / Related Issues

<!-- 关联的 Issue 编号，例如 Fixes #123、Closes #456、Related to #789；若无请填写 None。 -->
<!-- Related issue numbers, e.g. Fixes #123, Closes #456, Related to #789. Use "None" if not applicable. -->

## 变更类型 / Type of Change

<!-- 请在适用的选项前打勾。 / Please check all that apply. -->

- [ ] Bug fix (non-breaking change that fixes an issue)
- [ ] New feature (non-breaking change that adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to change)
- [ ] Documentation update
- [ ] Refactor or chore

## 截图 / Screenshots

> **必填 / Required.** 本插件的交付物是终端状态栏的展示效果，**修改前后的对比截图是 PR 审阅的必要材料**。
>
> **Required.** The core deliverable of this plugin is the visual output of the terminal status bar, so **before/after screenshots are mandatory for review**.
>
> 仅涉及非可视化逻辑（如配置解析、缓存策略、错误处理）、或仅包含文档修订 / `chore` 类变更的 PR，可在此处说明并附上测试输出或日志。
>
> PRs limited to non-visual logic (config parsing, caching, error handling), documentation updates, or `chore`-style changes may skip screenshots and instead attach test output or logs here.

### 修改前 / Before

<!-- 在此粘贴或上传修改前的截图。 -->
<!-- Paste or upload the screenshot of the original state here. -->

### 修改后 / After

<!-- 在此粘贴或上传修改后的截图。 -->
<!-- Paste or upload the screenshot of the new state here. -->

### 变更说明 / Notes

<!-- 简要说明上述截图之间的差异。 -->
<!-- Briefly describe the difference between the two screenshots. -->

## 测试 / Testing

请描述您为本次变更执行的测试。/ Please describe the testing you performed.

- [ ] 本地 `npm run build` 通过 / `npm run build` passes locally
- [ ] 在真实 Claude Code 环境中验证过插件输出 / Verified the plugin output in a real Claude Code session
- [ ] 补充说明 / Additional notes:

## 检查清单 / Checklist

- [ ] 代码遵循项目现有风格与目录结构 / Code follows the existing style and directory structure
- [ ] 公共函数与导出类型已添加 TSDoc 注释 / TSDoc comments added to public functions and exported types
- [ ] 未引入非必要的运行时依赖 / No unnecessary runtime dependencies added
- [ ] 提交信息遵循 Conventional Commits 规范 / Commit messages follow Conventional Commits
- [ ] PR 描述完整且包含必要的截图 / PR description is complete and includes the required screenshots (or an explicit exemption)
- [ ] 已审阅并处理 CodeRabbit 提出的所有建议 / Reviewed and addressed all CodeRabbit suggestions
