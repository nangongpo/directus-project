## 项目构建

1. 使用 mysql8.x 创建数据库 directus
  ```
  数据库名称：directus
  字符集：utf8mb4
  排序规则：utf8mb4_0900_ai_ci
  ```

2. npm init directus-project@latest 项目名称
  ```
  切换node环境为22

  Choose your database client MySQL / MariaDB / Aurora
  Port: 3306
  Database Name: directus
  Database User: root
  Database Password: 123456
  ```

3. "DB_CLIENT" Environment Variable is missing.
  ```
  环境变量文档：https://docs.directus.io/self-hosted/config-options/
  根目录创建.env
  ```

4. 项目初始化
  ```
  npx directus bootstrap
  npx directus start
  ```

5. 升级directus
  ```
  npm install directus@latest
  npx directus bootstrap
  npx directus start
  ```

6. Directus 数据库迁移命令
  ```
  运行所有待定的迁移
  npx directus database migrate:latest

  创建一个新的迁移文件
  npx directus database migrate:make <migration_name>

  显示所有迁移文件的状态
  npx directus database migrate:status

  回滚最近的一次迁移
  npx directus database migrate:rollback

  运行下一个待执行的迁移
  npx directus database migrate:up

  回滚最近的一个或 N 个已执行的迁移， 如回滚最近的 2 个迁移
  npx directus database migrate:down --step 2

  显示当前已执行的迁移版本
  npx directus database migrate:current
  ```
