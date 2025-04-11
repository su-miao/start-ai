# 概述
多功能 AI 智能体，支持代码执行、文件操作、网络搜索等任务。以完全开放的方式实现通用型 AI 代理功能。

官方代码库：[https://github.com/mannaandpoem/OpenManus](https://github.com/mannaandpoem/OpenManus)

# 前置要求
1. 公网可访问：要求目标 VPC 内可访问公网。
2. 大模型服务：要求有可用的大模型服务。

# 使用说明
1. 进入 OpenManus 部署页面，按照提示填写部署参数：

![](https://intranetproxy.alipay.com/skylark/lark/0/2025/png/312062/1744340282530-5198ff97-5c2c-4a81-b80c-223a15215f5d.png)

2. 应用部署依赖大模型服务：大模型名称、API Key、Endpoint，可从百炼获取
3. 部署成功后，在已部署场景中，可以跳转查看目标 OpenManus 应用 (该模板镜像较大，约12G，因此实例启动时间较长，约12分钟)

![](https://intranetproxy.alipay.com/skylark/lark/0/2025/png/312062/1744341637627-060771bf-61e4-4ecc-b4a3-8514849af0c9.png)

4. 验证与使用
    1. 登陆应用实例 webshell

![](https://intranetproxy.alipay.com/skylark/lark/0/2025/png/312062/1744340827296-ced4ff5a-aa03-4026-a6d5-e5a281729c99.png)

    2. 运行 python main.py，进入交互模式，输入 Prompt：<font style="color:rgb(42, 47, 69);">Help me write a research report on Alibaba Cloud SAE and save it as a Markdown file.</font>

![](https://intranetproxy.alipay.com/skylark/lark/0/2025/png/312062/1744341179432-59f463af-3d44-40b9-8339-01cf0a87fadc.png)

    3. 执行完成后，文件会默认保存在 workspace 目录下

![](https://intranetproxy.alipay.com/skylark/lark/0/2025/png/312062/1744342350837-6624cab3-efe4-4b96-8b1c-152ba3919e8e.png)

