#重新编译支持ARM64，感谢不懂和L原作者。 douniwan819/pansou-pancheck:latest

# PansouAndPanCheck

一个整合了 [pansou](https://github.com/fish2018/pansou) 搜索服务和 [PanCheck](https://github.com/Lampon/PanCheck) 链接有效性校验的代理服务。

## 功能特性

- 自动过滤无效的网盘链接，只返回有效链接
- 支持多种网盘平台（夸克、UC、百度、天翼、123云盘、115网盘、迅雷、阿里云等）
- 提供与原版 pansou 完全兼容的 API 接口
- 支持 POST 和 GET 请求方式
- 详细的过滤统计日志

## 部署方式

### Docker 部署（推荐）

```bash
docker run -d -p 1566:1566 \
  --name pansou-and-pancheck \
  -e SEARCH_API_URL=http://192.168.50.50:1514 \
  -e CHECK_API_URL=http://192.168.50.50:7024/api/v1/links/check \
  silent7897/pansou-and-pancheck:latest
```

### 环境变量说明

- `SEARCH_API_URL`：pansou 服务地址（默认值：http://127.0.0.1:8888）
- `CHECK_API_URL`：PanCheck 服务校验接口地址（默认值：http://127.0.0.1/api/v1/links/check）

### 本地部署

```bash
git clone https://github.com/your-repo/pansou-and-pancheck.git
cd pansou-and-pancheck
pip install -r requirements.txt
SEARCH_API_URL=http://your-pansou-url CHECK_API_URL=http://your-check-url python main.py
```

## 项目链接

- [pansou](https://github.com/fish2018/pansou)
- [pansou-web](https://github.com/fish2018/pansou-web)
- [PanCheck](https://github.com/Lampon/PanCheck)
