# db-sequelize-cli
db-sequelize-cli

## sequelize

+ 安装 ***sequelize-cli***

  ```
    npm install --save sequelize-cli sequelize mysql2
  ```

+ 生成 ***sequelize*** 目录

  ```
    node_modules/.bin/sequelize init

    // config：包含一个 config.json 文件
    // models：包含一个 index.js 文件
    // migrations：空文件夹
    // seeders：空文件夹
  ```

+ 修改 *config/config.json* 内容


+ 创建数据库

  ```
    node_modules/.bin/sequelize db:create
  ```

+ 生成模型文件和迁移文件

  ```
    node_modules/.bin/sequelize model:generate --name User --attributes firstName:string,lastName:string,email:string

    // 将 migrations *-create-user.js
    // 文件里的 createdAt 和 updatedAt 两个字段中的 allowNull 改成了 true

  ```

+ 执行迁移

  ```
  node_modules/.bin/sequelize db:migrate
  ```

+ 生成种子文件

  ```
    node_modules/.bin/sequelize seed:generate --name demo-user
  ```

+ 执行种子文件

  ```
    node_modules/.bin/sequelize db:seed:all
  ```