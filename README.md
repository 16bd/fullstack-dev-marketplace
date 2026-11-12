# Fullstack Dev

**Fullstack Dev 是一个面向中文开发团队的 Codex 全栈开发插件**，适用于 Web 前端、后端 API、前后端联调、通用脚本、代码审查和仓库审计。它沿现有代码和调用链定位问题，优先复用项目已有实现，并从页面、API 或脚本入口验证实际行为。

Fullstack Dev is a Codex plugin for Chinese-language web development, API debugging, code review, repository audits, and technical debt tracking.

[Codex Desktop 第三方插件安装教程](https://16bd.github.io/fullstack-dev-marketplace/) · [桌面端图文安装](#在-codex-desktop-安装) · [终端安装](#在终端安装) · [使用示例](#使用示例) · [常见问题](#常见问题)

## 在 Codex Desktop 安装

### 1. 打开「添加插件市场」

在 Codex Desktop 左侧打开 **插件**。点击插件页右上角的 **添加**，再选 **添加插件市场**。

![图 1：在插件页右上角打开「添加」菜单，选择「添加插件市场」](docs/images/desktop-1-add-marketplace.png)

### 2. 填写 GitHub 仓库地址

复制下面的地址，粘贴到 **来源**。**Git 引用**和**稀疏路径**都留空，然后点击右下角的 **添加市场**。

```text
https://github.com/16bd/fullstack-dev-marketplace.git
```

![图 2：把 GitHub 仓库地址粘贴到「来源」，点击「添加市场」](docs/images/desktop-2-enter-repository.png)

### 3. 搜索并安装 Fullstack Dev

回到插件页，在搜索框输入 **Fullstack Dev**。找到发布人为 **PFF** 的结果，点击右侧的 **＋**。如果列表里还没有这条结果，点击搜索框右侧的刷新图标再搜一次。

![图 3：找到发布人是 PFF 的 Fullstack Dev，点击条目右侧的加号](docs/images/desktop-3-install-plugin.png)

### 4. 开始使用

安装完成后，插件右侧的 **＋** 会变成 **⋯**。点击 **⋯ → 立即试用**，然后输入你要做的事。也可以新建一个 Codex 对话，直接输入需求。

> 给订单列表加状态筛选，并验证分页和清空筛选的行为。

![图 4：打开已安装插件的三点菜单，选择「立即试用」](docs/images/desktop-4-try-plugin.png)

## 在终端安装

```powershell
codex plugin marketplace add https://github.com/16bd/fullstack-dev-marketplace.git
codex plugin add fullstack-dev@fullstack-dev-marketplace
```

安装后打开一个新对话，即可试用下面的提示词。

## 使用示例

| 场景 | 可以直接输入的提示词 |
| --- | --- |
| 前端开发与验证 | 给订单列表加状态筛选，并验证分页和清空筛选的行为。 |
| API 排查与前后端联调 | 排查订单 API 返回空列表的问题，核对前端传参、接口默认值和分页行为。 |
| 数据库只读排查 | 排查某个订单为什么没出现在列表里。先说明查询范围，再用只读 SELECT 核对状态。 |
| 通用脚本开发 | 修复 CSV 汇总脚本，用一份正常输入和一份缺列输入验证输出和退出码。 |
| PR 和代码审查 | 审查当前 PR，按严重程度列出有代码证据的缺陷和回归风险。 |
| 仓库审计与技术债盘点 | 审计结算模块的调用链，并列出带 `shortcut:` 注释的技术债和升级条件。 |

## 常见问题

### 安装后需要手动选择 Fullstack Dev 吗？

可以直接描述需求，由 Codex 根据任务判断是否调用技能。要显式指定时，可以在输入框键入 `$`，搜索 `fullstack-dev` 并选择对应技能。

### Fullstack Dev 会执行数据库变更吗？

数据库排查只执行只读 `SELECT`，并在查询前说明目的和范围。涉及数据或表结构变更时，插件提供标明相关表和字段的 SQL，由你确认后自行执行。

### 可以只做代码审查或仓库审计吗？

可以。只要求审查、审计或技术债盘点时，插件会提交发现和代码证据，并保留工作区文件原样。具体流程可查看 [Fullstack Dev 技能说明](plugins/fullstack-dev/skills/fullstack-dev/SKILL.md)。

## 更新

```powershell
codex plugin marketplace upgrade fullstack-dev-marketplace
```

维护者将本目录的内容提交到 Git 仓库根目录，确保隐藏目录 `.agents/` 也已提交。更新插件时递增 `plugins/fullstack-dev/plugin.json` 中的版本号。
