# DataEyes Windows 一键安装使用教程

> 数眼智能 AI 助手一键部署工具，基于 [OpenClaw](https://github.com/nicepkg/openclaw) 开源项目。

## 下载

| 版本 | 说明 | 大小 |
|------|------|------|
| `openclaw.windows.exe` | 交互版（推荐） | 约 201MB |

下载地址：

- [OpenClaw Windows Installer (.exe)](https://github.com/dataeyesai/dataeyes-openclaw-windows-installer/releases/download/windows-installer-20260323/openclaw.windows.exe)

## 安装流程

双击运行 `.exe` 后，安装程序会自动完成以下步骤：

```text
[1/10]  创建目录
[2/10]  安装 Node.js 22
[3/10]  安装 Git
[4/10]  安装 OpenClaw
[5/10]  配置 API Key
[6/10]  获取可用模型列表
[7/10]  生成配置文件
[8/10]  安装本地代理
[9/10]  设置开机自启
[10/10] 启动服务并打开浏览器
```

## 配置 API Key

安装过程中会提示输入 API Key，支持同时配置两个站点：

```text
[1] 国内站
    国产 AI 模型：DeepSeek、通义千问、豆包、Kimi、智谱 GLM、MiniMax 等
    适合中国大陆用户，低延迟访问国产大模型
    获取 Key: https://www.shuyanai.com -> 登录账号 -> 控制台 -> API Key

    请输入国内站 API Key（sk-开头，回车跳过）:

[2] 国际站
    海外 AI 模型：Claude、GPT、Gemini、Grok 等
    一个 Key 统一调用全球顶尖 AI 模型
    获取 Key: https://www.dataeyes.ai -> 登录账号 -> 控制台 -> API Key

    请输入国际站 API Key（sk-开头，回车跳过）:
```

- 两个站点至少填写一个，也可以都填
- 填写完成后，安装程序会自动拉取当前 Key 可用的模型列表
- 安装完成后，可以在 WebUI 中自由切换模型

## 获取 API Key

| 站点 | 官网 | 适用模型 |
|------|------|----------|
| 国内站 | [www.shuyanai.com](https://www.shuyanai.com) | DeepSeek、通义千问、豆包、Kimi、智谱 GLM、MiniMax 等 |
| 国际站 | [www.dataeyes.ai](https://www.dataeyes.ai) | Claude、GPT、Gemini、Grok 等 |

获取步骤：

1. 打开官网
2. 登录账号
3. 进入控制台
4. 创建或复制 API Key

## 安装内容

安装包内含以下组件：

| 组件 | 版本 | 说明 |
|------|------|------|
| Node.js | 22.22.1 | JavaScript 运行环境 |
| OpenClaw | 2026.3.13 | AI 助手核心 |
| Git | 2.53.0 | 版本管理工具 |

## 安装完成后

- WebUI 地址：`http://127.0.0.1:18789`
- 配置文件：`%USERPROFILE%\.openclaw\openclaw.json`
- 开机自启：已自动配置，重启电脑后服务会自动运行
- 切换模型：在 WebUI 聊天界面中选择不同模型即可

## 系统要求

- Windows 10 / 11 / Server 2016+（64 位）
- 至少 500MB 可用磁盘空间
- 联网，用于验证 API Key 和获取模型列表

## 卸载

运行安装目录下的卸载脚本：

```text
%LOCALAPPDATA%\DataEyes\uninstall.bat
```

## 常见问题

### 报错 401 无效的令牌

请确认 API Key 与所选站点匹配：

- 国内站 Key 只能用于国内站 `shuyanai.com`
- 国际站 Key 只能用于国际站 `dataeyes.ai`

### 报错 503 No available channel

这表示当前模型在所选站点没有可用通道。可以：

- 在 WebUI 中切换为其他模型
- 再补充配置另一个站点的 Key

## 相关链接

- 数眼智能国内站：[www.shuyanai.com](https://www.shuyanai.com)
- 数眼智能国际站：[www.dataeyes.ai](https://www.dataeyes.ai)
- Windows 安装包 Release：[Windows Installer 2026-03-23](https://github.com/dataeyesai/dataeyes-openclaw-windows-installer/releases/tag/windows-installer-20260323)
