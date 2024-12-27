> [点我下载源码](https://www.oneprosol.com/detail/476bc90e21a34597963d8a8ff12a6305) 
> 或查看我的个人简介下载源码。
> 支持定制、讲解、修改、远程调试
### 一、相关技术

- 后端：`Java`、`JavaWeb` / `Springboot`。
- 前端：`Vue`、`HTML` / `CSS` / `Javascript` 。
- 数据库：`MySQL`

### 二、相关软件（列出的软件其一均可运行）

- `IDEA`
- `Eclipse`
- `Visual Studio Code(VScode)`
- `Navicat`
- 等

### 三、部署所需环境

- 后端：`jdk1.8`。
- 前端：`node`、`vue-cli` 、`npm`  。
- 数据库：`mysql5.7以上`

### 四、功能描述及功能图展示

系统分为：普通用户。

**普通用户功能：**

普通用户有登录、注册、论坛列表、论坛发布和论坛详情等功能

1. 登录
   ![1.登录.jpg](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-05%2012:22:47_1.%E7%99%BB%E5%BD%95.jpg)
2. 注册
   ![2.注册.jpg](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-05%2012:23:03_2.%E6%B3%A8%E5%86%8C.jpg)
3. 论坛列表
   ![3.论坛中心.jpg](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-05%2012:23:22_3.%E8%AE%BA%E5%9D%9B%E4%B8%AD%E5%BF%83.jpg)
4. 论坛发布
   ![4.发布论坛.jpg](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-05%2012:23:32_4.%E5%8F%91%E5%B8%83%E8%AE%BA%E5%9D%9B.jpg)
5. 论坛详情
   ![5.论坛详情.jpg](https://pic.picprosol.com/user_upload/1ca4a16527164fbdbe5588f4023765f3/2024-12-05%2012:23:42_5.%E8%AE%BA%E5%9D%9B%E8%AF%A6%E6%83%85.jpg)

### 五、数据库展示

```sql
SET NAMES utf8mb4;
SET FOREIGN_KEY_CHECKS = 0;

-- ----------------------------
-- Table structure for blink
-- ----------------------------
DROP TABLE IF EXISTS `blink`;
CREATE TABLE `blink`  (
  `id` varchar(32) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NOT NULL,
  `film_name` varchar(2000) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NULL DEFAULT NULL,
  `content` varchar(2000) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NULL DEFAULT NULL,
  `user_id` varchar(32) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NOT NULL,
  `director` varchar(2000) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NULL DEFAULT NULL,
  `genre` varchar(2000) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NULL DEFAULT NULL,
  `create_time` bigint(0) UNSIGNED NULL DEFAULT NULL,
  PRIMARY KEY (`id`) USING BTREE
) ENGINE = InnoDB CHARACTER SET = utf8mb3 COLLATE = utf8mb3_general_ci ROW_FORMAT = Dynamic;

DROP TABLE IF EXISTS `comment`;
CREATE TABLE `comment`  (
  `id` varchar(32) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NOT NULL,
  `content` varchar(2000) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NULL DEFAULT NULL,
  `user_id` varchar(32) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NOT NULL,
  `user_name` varchar(2000) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NULL DEFAULT NULL,
  `blink_id` varchar(32) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NOT NULL,
  `create_time` bigint(0) UNSIGNED NULL DEFAULT NULL,
  PRIMARY KEY (`id`) USING BTREE
) ENGINE = InnoDB CHARACTER SET = utf8mb3 COLLATE = utf8mb3_general_ci ROW_FORMAT = Dynamic;

DROP TABLE IF EXISTS `user`;
CREATE TABLE `user`  (
  `id` varchar(32) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NOT NULL,
  `account` varchar(2000) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NULL DEFAULT NULL,
  `password` varchar(2000) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NULL DEFAULT NULL,
  `mobile` varchar(2000) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NULL DEFAULT NULL,
  `name` varchar(2000) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NULL DEFAULT NULL,
  `create_time` bigint(0) UNSIGNED NULL DEFAULT NULL,
  PRIMARY KEY (`id`) USING BTREE
) ENGINE = InnoDB CHARACTER SET = utf8mb3 COLLATE = utf8mb3_general_ci ROW_FORMAT = Dynamic;
```
