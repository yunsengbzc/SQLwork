# 基本信息
链接：https://leetcode.cn/problems/find-customer-referee/description/?envType=study-plan-v2&envId=sql-free-50

# 题目描述
Customer
+-------------+---------+
| Column Name | Type    |
+-------------+---------+
| id          | int     |
| name        | varchar |
| referee_id  | int     |
+-------------+---------+
在 SQL 中，id 是该表的主键列。
该表的每一行表示一个客户的 id、姓名以及推荐他们的客户的 id。
找出那些 没有被 id = 2 的客户 推荐 的客户的姓名。

以 任意顺序 返回结果表。

结果格式如下所示。


# 思考
分析：没有被id = 2 的客户推荐的客户，即referee_id != 2的客户。并且要考虑referee_id为NULL的情况
考察点：基础（否定，NULL）

# 解法
```sql
select name
from Customer
where referee_id != 2 or referee_id = NULL

```