# xxl-job-modify

本项目为[xxl-job](http://www.xuxueli.com/xxl-job/)的修改本，针对自己的需求

## 使用示例:

```yaml
version: "3"
services:
  app:
    image: registry.cn-beijing.aliyuncs.com/codeforfun/xxl-job-modify:2.1.0
    environment:
      MYSQL_PASSWORD: root
    ports:
      - "8080:8080"
  mysql:
    image: mysql:5.7.26
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: root
    ports:
      - "3306:3306"
```

## 参数介绍:

名称 | 介绍 | 备注
---|---|---
image | registry.cn-beijing.aliyuncs.com/codeforfun/xxl-job-modify:2.1.0 | 最新版本latest，建议使用精确版本防止更新后被覆盖
SERVER_PORT | 容器内端口号 | 默认为8080
MYSQL_USERNAME | MySQL用户名 | 默认为 root
MYSQL_PASSWORD | MySQL密码 | 默认为 root_pwd
MYSQL_HOST | MySQL 地址 | 默认为 mysql
MYSQL_PORT | MySQL 端口号 | 默认为 3306
SPRING_MAIL_HOST | 邮件host | 默认为 smtp.qq.com
SPRING_MAIL_PORT | 邮件port | 默认为 25
SPRING_MAIL_USERNAME | 邮件用户名 | 默认为 xxx@qq.com
SPRING_MAIL_PASSWORD | 邮件密码 | 默认为 xxx

