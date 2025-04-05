# Gitea

Gitea 是一个轻量级的代码托管平台，内置了 CI/CD、项目管理和包管理。

## 配置

Gitea 分为两个部分，一个是 Gitea，一个是 Gitea Runner。

如果是配置 Gitea，可以参考 [Gitea 配置](https://docs.gitea.com/category/administration)。
如果是配置 Gitea Runner，可以参考 [Gitea Runner 配置](https://docs.gitea.com/usage/actions/overview)。

## 运行

首先把 `.env.example` 重命名为 `.env`，然后修改 `.env` 文件中的环境变量。

如果不需要CI/CD，可以只运行 Gitea：

```bash
docker compose -f docker-compose.gitea.yaml up -d
```

如果需要CI/CD，可以在运行上面的命令后再运行 Gitea Runner：

```bash
docker compose -f docker-compose.runner.yaml up -d
```

或者三个服务都运行：

```bash
docker compose -f ./docker-compose.gitea-with-runner.yaml up -d
```

## 注意事项

1. Gitea Runner 用到了配置 runner-config.yaml 文件，其中的 `container.network` 必须是 Gitea 的网络名称。
2. 可以在 `docker-compose.runner.yaml` 文件中的 `scale` 字段中设置 Gitea Runner 的数量。