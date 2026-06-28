# YoLuster Shorts 釉光影 Docker 本地部署包 v2.0.2

v2.0.2 是一次面向公开 Docker 本地前端体验包的品牌同步与稳定性修复更新。

本次更新重点不是新增一条大的产品功能主线，而是修复公开下载包中的旧品牌残留、优化包名版本识别，并强化本地前端瘦身包的发布校验。

## 主要更新

### 1. 品牌统一

- 公开本地前端包统一使用 `YoLuster Shorts 釉光影`。
- 修复旧 Logo 路径和旧品牌资源残留。
- 修复本地导出文件名中的旧 `yoyoung-shorts-local-*` 前缀。
- 保留必要的内部兼容协议字段，避免影响本地包与云端服务识别。

### 2. 本地包文件名版本化

旧包名 `docker-local-package-thin-bundle.zip` 不利于用户区分版本。

v2.0.2 起，推荐下载文件改为：

```text
yoluster-shorts-v2.0.2-docker-local-package-thin-bundle.zip
```

用户下载后可以直接从文件名识别版本，减少多个 zip 文件混在一起时的误用风险。

### 3. 本地前端包稳定性与安全边界校验

本次发布重新执行并加强了 Docker 前端瘦身包校验：

- 确认公开包仅包含前端静态文件、Nginx 代理模板和 Docker 启动文件。
- 确认不包含云端后端核心源码。
- 确认不包含数据库、密钥、生产配置或会员/中转等后端业务代码。
- 解压实物包后检查旧品牌可见文本与旧 Logo 文件残留。

### 4. 兼容性说明

本次没有改动云端后端业务逻辑，也没有改动登录、会员、额度、中转权限、OSS 存储区分等链路。

部分内部兼容字段仍会保留历史命名，这是为了避免影响本地前端包与云端后端之间已经存在的识别约定。

## 使用方式

1. 下载本版本中的 `yoluster-shorts-v2.0.2-docker-local-package-thin-bundle.zip`。
2. 解压到本地英文路径，例如：`D:\yoluster-shorts`。
3. 安装并启动 Docker Desktop。
4. 按压缩包内 README 配置 `.env` 并运行。
5. 在浏览器打开本地地址使用。

如果你已经部署过旧版本，建议先备份旧目录和个人配置，再解压新版本重新启动。

## 文件校验

下载文件：

```text
releases/v2.0.2/yoluster-shorts-v2.0.2-docker-local-package-thin-bundle.zip
```

SHA256：

```text
05BEE488BF37C2A35B027C13636442D06167A33B0CE3F80DB47CF7803F171150
```

