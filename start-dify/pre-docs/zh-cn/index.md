# 概述
Dify 是一个开源的 LLM 应用开发平台，是生成式 AI 应用创新引擎。直观的界面结合了 AI 工作流、RAG 管道、Agent、模型管理、可观测性功能等，从而可以快速从原型到生产。



官方代码库：[https://github.com/langgenius/dify](https://github.com/langgenius/dify)

# 前置要求
1. 公网可访问：要求目标 VPC 内可访问公网。
2. 阿里云 RDS 数据库：PostgreSQL 17 或其他产品。
3. 阿里云 Tair 数据库：Redis 开源版或 Tair 企业版。
4. 阿里云 AnalyticDB（pgvector）。
5. 阿里云 NAS 存储。

# 使用说明
1. 进入 Dify 社区版部署页面，按照提示填写相关部署参数

![](https://img.alicdn.com/imgextra/i1/O1CN01yaK9m41XcP47AjClo_!!6000000002944-0-tps-2240-1056.jpg)

2. Secret Key 用于安全签名以及加密数据库中的敏感信息，可以通过 'openssl rand -hex 16' 生成一个密钥，再在前缀添加 'sk-'  ，例如: 'sk-2d32e986bb9648a0c3655e85a2e8491b'

![](https://img.alicdn.com/imgextra/i4/O1CN01twtwZV2AAFjqQaGIG_!!6000000008162-2-tps-317-97.png)

3. 应用部署依赖阿里云 RDS 数据库地址，可以在 [阿里云 RDS 控制台](https://rds.console.aliyun.com/) 获取

![](https://img.alicdn.com/imgextra/i2/O1CN011A7s571V3Td98gDAY_!!6000000002597-0-tps-1673-1024.jpg)

4. 应用部署依赖阿里云 Tair 数据库地址，可以在 [阿里云 Tair 控制台](https://kvstore.console.aliyun.com) 获取

![](https://img.alicdn.com/imgextra/i3/O1CN01bzHFKR1LaJsFihDGv_!!6000000001315-0-tps-2028-764.jpg)

5. 应用部署依赖阿里云 AnalyticDB 数据库地址，可以在 [阿里云 AnalyticDB 控制台](https://gpdbnext.console.aliyun.com/gpdb/) 获取

![](https://img.alicdn.com/imgextra/i3/O1CN01OdeWyS1z184UNyLIc_!!6000000006653-0-tps-1772-685.jpg)

6. 部署成功后，在「Service 公网访问发布」的任务步骤中，可以获取到 Dify 应用的访问 IP

![](https://img.alicdn.com/imgextra/i4/O1CN0184foXI1EukE7nEZpA_!!6000000000412-0-tps-1024-750.jpg)

7. 同时，可以在已部署场景中，跳转查看目标 Dify 应用，进入 dify-nginx 应用获取公网访问地址

![](https://img.alicdn.com/imgextra/i2/O1CN01QzWddM1izj0Swzff7_!!6000000004484-0-tps-2096-682.jpg)

![](https://img.alicdn.com/imgextra/i1/O1CN0162GFfm1iXKS0UJ1PL_!!6000000004422-0-tps-1132-615.jpg)

![](https://img.alicdn.com/imgextra/i4/O1CN01OZBuL51j0dnY26C9Q_!!6000000004486-0-tps-1614-371.jpg)

# 验证与使用
1. 访问 Dify 公网访问地址，初次登陆会要求设置管理员账户

![](https://img.alicdn.com/imgextra/i2/O1CN01hzF1dF1CEUS9I7PEf_!!6000000000049-0-tps-656-610.jpg)

2. 设置完成管理员账户后，登录 Dify

![](https://img.alicdn.com/imgextra/i2/O1CN01Fuk75t1dqUwsb4tOf_!!6000000003787-0-tps-519-405.jpg)

3. 登录后就可以参考 [Dify 社区文档](https://github.com/langgenius/dify/blob/main/README_CN.md) 使用 Dify

![](https://img.alicdn.com/imgextra/i3/O1CN01BMWlZf1TYVEGuAxXJ_!!6000000002394-0-tps-1424-874.jpg)

![](https://img.alicdn.com/imgextra/i4/O1CN01j2v0jk1Rcxr5tTg1Z_!!6000000002133-0-tps-1139-1142.jpg)

# 注意事项
1. Redis 版本当前只支持支持 Redis 5.0 以及 Redis 6.0，不支持 Redis 7.0

![](https://img.alicdn.com/imgextra/i2/O1CN01PyFARy1iRphUsDXhp_!!6000000004410-2-tps-712-486.png)

2. Redis 密码中不支持包含 @ 以及 # 符号

![](https://img.alicdn.com/imgextra/i4/O1CN01rxMDPX1pnXmmESFP5_!!6000000005405-2-tps-624-206.png)

3. RDS 需要创建账号类型为 高权限账号 的账号

![](https://img.alicdn.com/imgextra/i2/O1CN01p5kZFm1kGV8FJcJ2F_!!6000000004656-2-tps-741-587.png)

4. RDS 数据库需要先提前创建好 dify 数据库，并授权给之前创建的 高权限账号

![](https://img.alicdn.com/imgextra/i1/O1CN01ILCKQC1Z1QJvuzoFa_!!6000000003134-2-tps-718-624.png)
解释


