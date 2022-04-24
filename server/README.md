Code of the MySQL protocol and connection management.

MySQL协议和连接管理的代码。

目的是管理客户端连接，解析MySQL命令并返回执行结果。
具体实现根据MySQL协议，可以参考MySQL客户机/服务器协议文档。
如果需要在项目中使用MySQL协议解析和处理功能，可以参考本模块。
连接建立的逻辑在server的Run()方法中

```go

conn, err := s.listener.Accept()
clientConn := s.newConn(conn)
go s.onConn(clientConn)

```


tidb/sever
协议层和SQL层之间的接口

tidb/parser
SQL解析和语法分析

tidb/planner
验证、查询计划构建、查询计划优化

tidb/executor
执行

tidb/distsql
通过TiKV客户端向TiKV发送请求，并汇总返回结果。

tidb/kv
KV客户端接口

tikv/client-go
TiKV Go客户端
