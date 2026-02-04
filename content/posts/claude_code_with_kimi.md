+++
date = '2026-02-03T23:44:47+08:00'
draft = false
title = 'Claude Code 国内极简手册 (2026)'
+++

Claude Code 是 Anthropic 推出的终端 AI 助手。通过以下配置，国内用户可无缝接入 Kimi 和 DeepSeek。

# 极速安装

- 环境：需安装 Node.js 18+。

- 命令：在终端执行：
```bash
npm i -g @anthropic-ai/claude-code
```

## 接入 DeepSeek / Kimi

Claude Code 默认连接官方接口。国内使用需通过环境变量重定向至国产模型。

### 接入 Kimi（推荐， 目前kimi2.5效果可媲美opus））


### 接入 DeepSeek

DeepSeek 提供了 Anthropic 兼容接口，配置最简单。

- 获取 Key：platform.deepseek.com

- 设置变量（在终端执行）：
```bash
export ANTHROPIC_BASE_URL="https://api.deepseek.com/anthropic"
export ANTHROPIC_AUTH_TOKEN="你的_DeepSeek_Key"
export ANTHROPIC_MODEL="deepseek-chat"
```


# 快速启动

在代码项目根目录下直接输入：

```bash
claude
```