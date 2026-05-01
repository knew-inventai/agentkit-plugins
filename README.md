# agentkit-plugins

AgentKit Plugins 集合。每個子目錄為一個 plugin package。

## 安裝（Claude Code）

```shell
/plugin marketplace add knew-inventai/agentkit-plugins
/plugin install PLUGIN_NAME@agentkit-plugins
```

## 目錄結構

```
agentkit-plugins/
  .claude-plugin/
    marketplace.json    ← Claude Code marketplace 定義（自動維護）
  {plugin-name}/
    plugin.json         ← Package metadata
    README.md           ← 說明文件
```
