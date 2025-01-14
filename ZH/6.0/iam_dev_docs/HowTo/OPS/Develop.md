# 开发测试环境搭建

接入系统在正式接入权限中心前，会在开发者本地环境进行开发及联调；

此时，`切勿直接使用生产环境的IAM`进行对接；

应该:

1. 搭建一套独立的`开发测试环境`，同`生产环境`隔离；
2. 这套环境需要同`生产环境`版本一致，包含`PaaS/ESB/用户管理/权限中心SaaS /权限中心后台`等
3. 开发者可以通过地址访问这套环境的`权限中心SaaS`及`权限中心后台`； 通过`权限中心SaaS`配置权限，通过`权限中心后台`接口进行鉴权等
4. 这套环境只用于`开发测试`，所有数据随时可以清空重建；
 

## 本地开发步骤

1. 阅读文档，理解权限中心相关概念/接口/协议等
2. 确认`开发测试环境`的 paas 地址/iam 后台访问地址/iam saas 地址等
3. 分析系统权限模型，梳理好权限模型后，可以直接使用 [模型自动初始化及更新 migration](../Migration.md) 脚本导入`开发测试环境`
4. 此时可以到`权限中心SaaS`申请及配置相关权限
5. 调用接口，进行鉴权测试
6. 可以阅读相关 sdk 文档，使用 sdk 进行接入 [Python SDK](../../Reference/SDK/01-PythonSDK.md)
