# JetBrains Youtrack

[YouTrack](https://www.jetbrains.com/youtrack/) 是 JetBrains 公司推出的一款用于项目管理的工具，它提供了丰富的功能来帮助团队管理和跟踪项目进度。

## 配置

可以在 `.env` 文件中配置以下环境变量：

- `YOUTRACK_VERSION`：YouTrack 的版本号。
- `YOUTRACK_PORT`：YouTrack 的端口号。
- `YOUTRACK_BASE_DIR`：YouTrack 运行的根目录。

## 运行

可以通过以下命令运行 YouTrack：

```bash
docker compose up -d
```

## 访问

运行后可以通过指定的端口访问，默认为5080，即 http://localhost:5080。如果使用了
OrbStack，还可以通过 https://youtrack.local 访问。
