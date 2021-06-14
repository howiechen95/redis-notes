# 介绍
redis 是使用内存存储的非关系型数据库(key-value)
特点：
1 基于内存
2 支持主从复制特性
3 相比memcached,支持更多的数据结构以及操作
4 相比关系型数据库，避免写入不必要的临时数据


# 数据结构
1 基本数据类型
字符串、列表、集合、散列表、有序集合
string,list,set,hash,zset
每种数据结构有专属命令，支持批量操作、不完全的事务支持

string 字符串
get/set/del

list 链表
rpush [key] [value] // 推入列表右边
lrange [key] [startIndex] [endIndex] // 列出指定列表索引的值,-1为结束索引
LINDEX [KEY_NAME] [INDEX_POSITION] // 列出指定单个key  
lpop [key]  // 从列表左端弹出一个元素

set 集合
sadd [key] [item]
smembers [key] // 获取集合元素
sismember [key] [item] // 判断 item 是否在 key 的集合中
srem [key] [item] // 移除集合 key 中的 item，结果返回被移除数量

hash 哈希
hset [hkey] [key] [value] // 将 key-value 写入 hkey 中
hgetall [hkey] // 获取 hkey 中所有 key-value
hdel [hkey] [key] // 删除 hkey 中 的 key-value

zset 有序集合
zadd [key] [score] [value] // 集合中添加分值为 score 的 key-value  
zrange [key] [startIndex] [endIndex] (withscores) // 列出指定列表索引的值,-1为结束索引  withscores 为结果返回分值
zrangescore [key] [minScore] [maxScore] (withscores) // 根据分值列出指定列表索引的值 ,withscores  为结果返回分值
zrem [key] [value] // 移除

高级特性：
发布订阅、主从复制、持久化、脚本、存储过程

# web应用案例


# redis 命令

# 数据安全和性能(高可用)

# 应用

# 内存使用优化

# Lua脚本

