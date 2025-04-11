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

![](https://intranetproxy.alipay.com/skylark/lark/0/2025/png/168355/1744345314758-640841da-1564-41ec-88ab-672357d88203.png)

2. 应用部署依赖阿里云 RDS 数据库地址，可以在 [阿里云 RDS 控制台](https://rds.console.aliyun.com/) 获取

![](https://intranetproxy.alipay.com/skylark/lark/0/2025/png/168355/1744345531335-28de5a9f-1724-403c-b4c7-1de1c5e0c343.png)

3. 应用部署依赖阿里云 Tair 数据库地址，可以在 [阿里云 Tair 控制台](https://kvstore.console.aliyun.com) 获取

![](https://intranetproxy.alipay.com/skylark/lark/0/2025/png/168355/1744345660246-fee44880-7a38-4e96-882b-45a9f487123c.png)

4. 应用部署依赖阿里云 AnalyticDB 数据库地址，可以在 [阿里云 AnalyticDB 控制台](https://gpdbnext.console.aliyun.com/gpdb/) 获取

![](https://intranetproxy.alipay.com/skylark/lark/0/2025/png/168355/1744345804555-ef332bb0-177e-498c-b6dd-a357384479c8.png)

5. 部署成功后，在「Service 公网访问发布」的任务步骤中，可以获取到 Dify 应用的访问 IP

![](https://intranetproxy.alipay.com/skylark/lark/0/2025/png/168355/1744345939924-135c3586-141f-4894-be96-da9840f3f293.png)

6. 同时，可以在已部署场景中，跳转查看目标 Dify 应用，进入 dify-nginx 应用获取公网访问地址

![](https://intranetproxy.alipay.com/skylark/lark/0/2025/png/168355/1744346002207-3df51e69-3a56-465b-bb4a-204f011eea64.png)

![](https://intranetproxy.alipay.com/skylark/lark/0/2025/png/168355/1744346048377-50968f54-b6e1-4018-b67d-ac911b765b3b.png)

![](https://intranetproxy.alipay.com/skylark/lark/0/2025/png/168355/1744346068396-6597651b-458b-47c7-86fd-24e364e3d1e7.png)

# 验证与使用
1. 访问 Dify 公网访问地址，初次登陆会要求设置管理员账户

![](https://intranetproxy.alipay.com/skylark/lark/0/2025/png/168355/1744346218480-fd097fb5-692c-49a3-9bd2-e2c264e06f0d.png)

2. 设置完成管理员账户后，登录 Dify

![](https://intranetproxy.alipay.com/skylark/lark/0/2025/png/168355/1744346255071-bf175ad5-6ac3-474f-b574-925126c97427.png)

3. 登录后就可以参考 [Dify 社区文档](https://github.com/langgenius/dify/blob/main/README_CN.md) 使用 Dify

![](https://intranetproxy.alipay.com/skylark/lark/0/2025/png/168355/1744346358447-e66e86d5-09a3-4a08-bf22-137c1cc36871.png)

![](https://intranetproxy.alipay.com/skylark/lark/0/2025/png/168355/1744346459720-ecf70cf0-088a-48f1-b043-63acc205ca6b.png)



