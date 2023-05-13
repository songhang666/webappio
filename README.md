# webapp.io-deploy

<https://webapp.io/{你的GitHub用户名}/deployments>

点 `Deploy a new site` 按钮 下载你 `fork`的本项目部署

## 环境变量说明

Nezha 的端口设置为 443 就会自动加 --tls

```env
SECRET ENV ARGO_AUTH      # Argo 项目的认证信息TOKEN
SECRET ENV ARGO_DOMAIN    # Argo 访问项目的域名
SECRET ENV NEZHA_KEY      # Nezha 的 key 
SECRET ENV NEZHA_PORT     # Nezha 的服务端口
SECRET ENV NEZHA_SERVER   # Nezha 的服务地址
SECRET ENV PORT           # 容器内服务的端口 一般设置 3000
SECRET ENV TARGET_HOSTNAME_URL # 代理目标主机的网址 不使用 v2board 设置 http://127.0.0.1:8081
SECRET ENV MAX_MEMORY_RESTART # PM2重启时的内存阈值
# 以下为 v2board 相关配置
SECRET ENV API_HOST       # v2board API 服务的域名URL
SECRET ENV API_KEY        # v2board API 的 access key
SECRET ENV CERT_DOMAIN    # v2board 证书的域名
SECRET ENV NODE_ID        # v2board 节点 ID
```

## 选择添加

```env
SECRET ENV SSH_PUB_KEY # 设置Public Key 用于ssh连接 一般不需要设置 除非你需要ssh连接 ssh-rsa AAAAB3NzaC1yc2EAAA...
SECRET ENV TUNNEL_TRANSPORT_PROTOCOL # 设置cloudflared 传输协议 默认为 quic 可选 http2
```
