# 本地翻译工作台（Translation Workbench）

基于 **Ollama + HY-MT1.5-1.8B** 的中英互译网页工具，单文件、无后端、流式输出。

## 功能

- 整段翻译（**流式输出**，边生成边显示，可随时停止）
- 逐行批量翻译（并发 3）
- 术语干预（强制指定词汇译法，如"褶皱 → wrinkle effects"）
- 翻译历史（本地浏览器保存）
- 可配置 Base URL / 模型名 / API Key，兼容 Ollama 原生与 OpenAI 兼容接口
- 中英日韩目标语言、交换原文译文、复制译文

## 使用前提

1. 本机安装 [Ollama](https://ollama.com/) 并拉取翻译模型：
   ```bash
   ollama pull sun_leaf/HY-MT:1.8b
   ```
2. 允许浏览器跨域访问本地 Ollama（设置环境变量后重启 Ollama）：
   ```
   OLLAMA_ORIGINS=*
   ```
3. 打开本页面（GitHub Pages 或本地双击打开均可）。

## 部署到自己的 GitHub Pages

1. Fork 本仓库
2. 仓库 Settings → Pages → Source 选 `main` 分支 `/` 根目录
3. 访问 `https://<你的用户名>.github.io/translation-workbench/`

## 说明

- 翻译在本地完成，数据不出本机（模型推理在 Ollama 本地服务中进行）
- 配置项（Base URL / 模型 / Key）保存在浏览器 localStorage
- API Key 为明文存储，仅限本人电脑使用
