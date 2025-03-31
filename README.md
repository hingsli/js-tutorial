## 🖥️ 本地部署指南

1. 配置国内npm镜像（加速安装）
```bash
npm config set registry https://registry.npmmirror.com
```

2. 安装依赖环境
```bash
npm install -g docsify-cli
```

3. 克隆仓库并启动服务
```bash
git clone https://github.com/hingsli/js-tutorial.git
cd docs
docsify serve
```

4. 浏览器访问
```
http://localhost:3000
```

> 提示：若端口冲突可使用 `docsify serve -p 新端口号`
