# 概述
多功能 AI 智能体，支持代码执行、文件操作、网络搜索等任务。以完全开放的方式实现通用型 AI 代理功能。

官方代码库：[https://github.com/mannaandpoem/OpenManus](https://github.com/mannaandpoem/OpenManus)

# 前置要求
1. 公网可访问：要求目标 VPC 内可访问公网。
2. 大模型服务：要求有可用的大模型服务。

# 使用说明
1. 进入 OpenManus 部署页面，按照提示填写部署参数：

![](https://img.alicdn.com/imgextra/i3/O1CN01Yp38jc1CRlwNkCJjI_!!6000000000078-0-tps-4570-1354.jpg)

2. 应用部署依赖大模型服务：大模型名称、API Key、Endpoint，可从百炼获取
3. 部署成功后，在已部署场景中，可以跳转查看目标 OpenManus 应用 (该模板镜像较大，约12G，因此实例启动时间较长，约12分钟)

![](https://img.alicdn.com/imgextra/i2/O1CN01EsHcBu1suovGMCabY_!!6000000005827-0-tps-4566-1018.jpg)

# 验证与使用
1. 登陆应用实例 webshell

![](https://img.alicdn.com/imgextra/i3/O1CN01VteaDi1QfQMp9E8Sq_!!6000000002003-0-tps-5042-1238.jpg)

2. 运行 python main.py，进入交互模式，输入 Prompt：Help me write a research report on Alibaba Cloud SAE and save it as a Markdown file.

![](https://img.alicdn.com/imgextra/i1/O1CN011mvOkU1JKAg5nZgeD_!!6000000001009-0-tps-5104-1744.jpg)

3. 执行完成后，文件会默认保存在 workspace 目录下

![](https://img.alicdn.com/imgextra/i3/O1CN011yjWBp1dJ42HYuOSy_!!6000000003714-0-tps-2412-622.jpg)

