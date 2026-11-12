# Fullstack Dev

用于前端、后端、联调和脚本开发，也支持代码审查、仓库审计和技术债盘点。

## 安装

1. 在终端运行以下命令，添加这个市场来源。

   ```powershell
   codex plugin marketplace add https://github.com/16bd/fullstack-dev-marketplace.git
   ```

2. 重启 Codex 桌面端，打开「插件」，选择 **Fullstack Dev** 市场来源，再点开 **Fullstack Dev** 插件并安装。
3. 打开一个新对话，直接描述开发任务。例如「给订单列表加状态筛选，并验证分页和清空行为」。

也可以在终端安装插件。

```powershell
codex plugin add fullstack-dev@fullstack-dev-marketplace
```

## 更新

```powershell
codex plugin marketplace upgrade fullstack-dev-marketplace
```

维护者将本目录的内容提交到 Git 仓库根目录，确保隐藏目录 `.agents/` 也已提交。更新插件时递增 `plugins/fullstack-dev/plugin.json` 中的版本号。
