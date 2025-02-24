# Grok Chat Proxy

一个用于代理 Grok AI 聊天的服务，支持 OpenAI API 格式。

## 一键部署到 Render

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy?repo=https://github.com/fuwei99/grok_chat_proxy)

## 部署步骤

1. Fork 这个仓库到你的 GitHub 账号

2. 点击上方的 "Deploy to Render" 按钮

3. 在 Render 中连接你的 GitHub 账号并选择刚才 fork 的仓库

4. 部署完成后，你会得到一个类似 `https://your-app-name.onrender.com` 的域名

5. 修改你的 config.json 文件，添加你的 Grok cookies

## 使用方法

部署完成后，你可以使用任何支持 OpenAI API 的客户端，将 API 地址改为你的 Render 域名即可。

例如：
```bash
curl https://your-app-name.onrender.com/v1/chat/completions \
  -H "Content-Type: application/json" \
  -d '{
    "model": "grok-3",
    "messages": [{"role": "user", "content": "Hello!"}]
  }'
