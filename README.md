# Global Science Magazine — 组织级文档与配置

本仓库存放数字业务部的团队规范、协作模板和组织级配置，适用于 Global-Science-Magazine organization 下的所有项目。

本仓库为 **public**，内容对外可见。请勿在此提交任何敏感信息。

## 文档

| 文件 | 说明 |
| --- | --- |
| [技术管理规范.md](技术管理规范.md) | 部门技术管理规范（试行版），涵盖职责边界、文档要求、项目流程、AI 工具责任等 |
| [CODEOWNERS](CODEOWNERS) | 代码所有者配置，所有文件变更须经指定 code owner review 后才能合并 |
| [ISSUE_TEMPLATE/bug-report.md](ISSUE_TEMPLATE/bug-report.md) | Issue 模板：问题报告 |
| [ISSUE_TEMPLATE/task.md](ISSUE_TEMPLATE/task.md) | Issue 模板：任务提报 |
| [PULL_REQUEST_TEMPLATE.md](PULL_REQUEST_TEMPLATE.md) | PR 模板 |

## 协作规范

本组织下所有仓库均采用统一的协作流程：

- **`main` 分支受保护**：不接受直接推送，不允许 force push，不允许删除分支
- 所有修改须通过 Pull Request 合并，且必须经 code owner approve 后才能合并

> **关于技术强制**：public 仓库（`.github`、`frontend`）已通过 branch protection + CODEOWNERS 做到技术强制。private 仓库（`team-ops`、`migration-playbook`）受当前 GitHub Free 方案限制，暂时无法开启分支保护，**上述规则完全依赖团队成员自觉遵守**，跪请不要违反。
- 分支命名：`feature/描述`、`fix/描述`、`docs/描述`
- Commit message 格式：`type: 简要描述`（type 取值：`feat` / `fix` / `docs` / `chore` / `refactor`）

> 各仓库如有额外要求，以仓库内 README 为准。

**⚠️ 严禁提交敏感信息**：API 密钥、Token、`.env` 文件、数据库密码等不得出现在任何 commit 中。详见[技术管理规范 §四](技术管理规范.md#四敏感信息管理)。

## Issue 和 PR 模板

本仓库提供组织级默认模板，适用于所有未单独配置模板的仓库。如果某个仓库有自己的模板，以该仓库的模板为准，组织默认模板不会生效。

**在 ONES 上提交的需求和缺陷，请遵照以下模板。**

### Issue 模板

创建 issue 时会看到两个模板选项：

| 模板 | 用途 | 文件 |
| --- | --- | --- |
| 问题报告 | 报告异常行为或缺陷 | [ISSUE_TEMPLATE/bug-report.md](ISSUE_TEMPLATE/bug-report.md) |
| 任务提报 | 提交工作任务或待办事项 | [ISSUE_TEMPLATE/task.md](ISSUE_TEMPLATE/task.md) |

请按模板结构填写，不要删除段落标题。这条要求同样适用于 PR 模板。

### PR 模板

创建 PR 时描述框会自动填充模板，包含三个部分：

| 段落 | 填写要求 |
| --- | --- |
| 改动说明 | 写清改了什么、为什么改 |
| 关联议题 | 用 `Fixes #N` 关联 issue |
| 验证方式 | 写清审核人怎么确认改动是对的 |

模板文件：[PULL_REQUEST_TEMPLATE.md](PULL_REQUEST_TEMPLATE.md)

