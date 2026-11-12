# Fullstack Dev

用于前端、后端、联调和脚本开发，也支持代码审查、仓库审计和技术债盘点。

## 在 Codex Desktop 安装

首次安装时，在终端添加 GitHub 市场来源。已添加过的用户可以直接打开插件页。

```powershell
codex plugin marketplace add https://github.com/16bd/fullstack-dev-marketplace.git
```

1. 重启 Codex Desktop，打开侧栏的 **插件（Plugins）**。
2. 在搜索框右侧的市场下拉菜单里，选择 **Fullstack Dev**。
3. 找到 **Fullstack Dev** 插件，点击右侧的 **＋** 安装。

![Codex Desktop 插件页，搜索框右侧是市场下拉菜单，插件条目右侧是加号安装按钮](https://developers.openai.com/images/codex/plugins/codex-local-plugin-light.png)

*截图来自 OpenAI 官方文档。图中的市场和插件是示例，安装时请选择 **Fullstack Dev**。* [查看原图所在的文档](https://developers.openai.com/plugins/build/plugins#build-your-own-curated-plugin-list)

安装后，在插件页的 **已安装（Installed）** 区域确认 **Fullstack Dev** 已出现。新建一个 Codex 对话，就可以直接描述开发任务，例如「给订单列表加状态筛选，并验证分页和清空行为」。

## 在终端安装

```powershell
codex plugin marketplace add https://github.com/16bd/fullstack-dev-marketplace.git
codex plugin add fullstack-dev@fullstack-dev-marketplace
```

## 更新

```powershell
codex plugin marketplace upgrade fullstack-dev-marketplace
```

维护者将本目录的内容提交到 Git 仓库根目录，确保隐藏目录 `.agents/` 也已提交。更新插件时递增 `plugins/fullstack-dev/plugin.json` 中的版本号。
