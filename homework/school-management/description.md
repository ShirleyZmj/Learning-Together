# 全栈作业
## 背景描述
一个私立教育机构需要一个系统来执行一些行政功能，管理员可以跟踪教师及其课程。
你的任务是开发一个全栈应用程序来帮助管理员。屏幕和API的详细信息在下面的任务中。对于本次练习，你不需要实现登录和访问控制。

## 要求和期望
- 你的代码应上传到公开可访问的Github（或其他类似服务）仓库。
- （可选）将你的Web应用程序和API部署到一个公开可访问的托管环境。
- 你的代码库应包含一个`README.md`，其中包括以下内容：
  - 清晰的说明，如何运行本地实例的Web应用程序和API服务器以进行测试和评估
  - 清楚地记录所做的假设
  - 托管的Web应用程序和API的链接（如果适用）
  - （可选）对API设计的输入/建议
- 在前端和后端使用单一语言（仅允许TypeScript或JavaScript）。
- 使用NodeJS作为后端运行时环境。
- 前端使用React库。
- 强烈推荐使用关系型数据库。你可以使用PostgreSQL、MySQL或MariaDB。
- 允许使用第三方库（例如Ant Design或Material UI）。
- 前端屏幕的实现不必与提供的Figma设计完全一致。然而，你的应用程序应具有相同的用户流程和输入控件。
- （可选）包括单元测试。

## 重要！
我们将全面评估你的提交（即不仅仅是功能方面），包括以下因素：
- 可读性和代码整洁性
- 安全编码实践
- 代码结构/设计，例如模块化、可测试性
- 你的API可能会被自动化测试工具测试，因此请严格遵循给定的规格。
- （可选）你可以为已实现的API提供Postman集合，但我们可能仍会使用我们自己的工具来测试你的API。

## 任务
1. 作为管理员，我希望在系统中注册一名教师。
API

端点：POST /api/teachers
头部：Content-Type: application/json
成功响应状态：HTTP 201
请求体示例：
```json
{
  "name": "Mary",
  "subject": "Mathematics",
  "email": "teachermary@gmail.com",
  "contactNumber": "68129414"
}
```

1. 作为管理员，我希望检索系统中的教师列表。
设计：Figma屏幕

API

端点：GET /api/teachers
成功响应状态：HTTP 200
成功响应体：
```json
{
  "data" :
    [
      {
        "name": "Mary",
        "subject": "Mathematics",
        "email": "teachermary@gmail.com",
        "contactNumber": "68129414"
      },
      {
        "name": "Ken",
        "subject": "Mother Tongue Language",
        "email": "teacherken@gmail.com",
        "contactNumber": "61824191"
      }
    ]
}
```

3. 作为管理员，我希望添加一个新班级并指定班主任。
注意：一名教师只能是一个班级的班主任。

设计：Figma屏幕

API

添加班级
端点：POST /api/classes
头部：Content-Type: application/json
成功响应状态：HTTP 201
请求体示例：
```json
{
  "level": "Primary 1",
  "name": "Class 1A",
  "teacherEmail": "teachermary@gmail.com"
}
```

4. 作为管理员，我希望检索系统中的班级列表。
设计：Figma屏幕

API

端点：GET /api/classes
成功响应状态：HTTP 200
成功响应体：
```json
{
  "data" :
    [
      {
        "level": "Primary 1",
        "name": "Class 1A",
        "formTeacher": {
          "name": "Mary"
        }
      },
      {
        "level": "Primary 2",
        "name": "Class 2B",
        "formTeacher": {
          "name": "Ken"
        }
      }
    ]
}
```

## 错误处理
对于上述所有API端点，错误响应应：

- 具有适当的HTTP响应代码（例如400）
- 具有包含有意义错误消息的JSON响应体，格式如下：
```json
{ "error": "一些有意义的错误信息" }
```

## 设计稿
![设计稿](./ui-design.png)