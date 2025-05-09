# 数据库

## 群里提到的数据库
### **不同数据库对比表格（存储架构、应用场景、查询方式）**  

| **数据库**        | **类型**                  | **存储方式**            | **分布式支持** | **主要应用场景**                                       | **查询方式** |
|------------------|--------------------------|----------------------|----------------|------------------------------------------------|--------------|
| **SQLite**       | 关系型（嵌入式）          | 单文件存储           | ❌（单机）      | 移动端/小型应用，离线存储                        | SQL          |
| **PostgreSQL**   | 关系型（OLTP）           | 磁盘存储（B+树索引） | ❌（单机）/✅（分布式扩展，如 Citus） | 事务性数据库，企业应用                           | SQL          |
| **MySQL**        | 关系型（OLTP）           | 磁盘存储（B+树索引） | ❌（单机）/✅（MySQL Cluster） | 事务性数据库，Web 开发                         | SQL          |
| **BigQuery**     | 云数据仓库（OLAP）       | 分布式存储（GCP）    | ✅（Google Cloud） | 大数据分析，BI 报告                            | SQL          |
| **Hive**         | 数据仓库（OLAP）         | HDFS（列存储）       | ✅（Hadoop 生态） | 大规模数据分析（批处理）                         | SQL（HiveQL） |
| **ClickHouse**   | 列式数据库（OLAP）       | 磁盘存储（列存）     | ✅（分布式支持）  | 实时数据分析，日志分析                          | SQL          |
| **HBase**        | NoSQL（列存数据库）      | HDFS（LSM-Tree）     | ✅（Hadoop 生态） | 高吞吐 OLAP，时序数据存储                      | NoSQL（KV）  |
| **Druid**        | OLAP 数据库              | 分布式存储（列存）   | ✅（分布式支持）  | 实时数据分析，流式数据处理                      | SQL（Druid SQL） |
| **Redis**        | NoSQL（KV 存储）         | 内存数据库（可持久化） | ✅（Redis Cluster） | 高速缓存，消息队列，会话管理                   | NoSQL（KV）  |
| **PgSQL HashData** | 分布式 PostgreSQL      | 磁盘存储（B+树索引） | ✅（分布式存储）  | 分布式事务，金融级应用                         | SQL          |
| **Oracle**       | 关系型（OLTP/OLAP）      | 磁盘存储（B+树索引） | ✅（Oracle RAC） | 企业级事务系统，银行、政府                     | SQL          |

---

### **总结**
1. **OLTP（在线事务处理）**：
   - 适用于高并发、低延迟的事务型业务，如用户登录、订单处理、支付系统。
   - 代表数据库：**MySQL、PostgreSQL、Oracle**。
  
2. **OLAP（在线分析处理）**：
   - 适用于大规模数据分析，通常用于 BI（商业智能）和报表分析。
   - 代表数据库：**Hive、ClickHouse、BigQuery、Druid**。

3. **NoSQL & KV 存储**：
   - 适用于高吞吐、大规模数据，如缓存、日志、时序数据库。
   - 代表数据库：**HBase、Redis**。

4. **数据仓库 & 分布式计算**：
   - 适用于大数据分析、批处理计算。
   - 代表数据库：**Hive、BigQuery、ClickHouse**。


## 研究kv存储
- [rosedb](https://github.com/rosedblabs/rosedb)
- [bitcask](https://github.com/bitcask/bitcask)
- [lsm-tree](https://github.com/facebook/rocksdb)
- [bbolt](https://github.com/etcd-io/bbolt)

## 学术圈分享
【易百分同学】我主要是搞键值存储的，也算是数据库中的存储引擎，跟实际的数据库产品还是有点差距。存储引擎我主要在搞LSM-tree，工业级的推文比较我也不是了解，但论文里面经常会提到的工业级的系统。比如说LSM-tree的工业级产品facebook的rocksDB，阿里的X-engine，polarDB，PingCap的TiDB，Apache的Cassandra，Google的LevelDB。
- https://cassandra.apache.org/_/index.html
- https://docs.pingcap.com/zh/tidb/stable/overview/
- https://help.aliyun.com/zh/rds/apsaradb-rds-for-mysql/x-engine/
- https://help.aliyun.com/zh/polardb/product-overview/
- https://engineering.fb.com/2013/11/21/core-infra/under-the-hood-building-and-open-sourcing-rocksdb/