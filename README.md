# 业务督导中心数智化平台门户

Vue3 + Vite 纯前端单页门户项目，用作业务督导中心数智化平台统一入口。

部署域名规划：https://home.ywddzx.com

## 开发

```bash
npm install
npm run dev
```

## 构建

```bash
npm run build
```

构建产物位于 `dist` 目录，可通过 Nginx 静态托管。

## Docker 部署

构建镜像：

```bash
docker build -t ywddzx-home-portal .
```

启动容器：

```bash
docker run -d --name ywddzx-home-portal -p 5170:5170 ywddzx-home-portal
```

或使用 Docker Compose：

```bash
docker compose up -d --build
```

访问地址：http://127.0.0.1:5170/
