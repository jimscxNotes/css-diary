## html5 中的webSql
### 三个核心方法
1. openDatabase     使用现有数据库，或者是创建新的数据库
    接受五个参数，依次是:
    * 数据库名字
    * 版本
    * 显示的数据库名
    * 数据库大小，
    * 回调函数（可以不设置）

    ```
    var db = openDatabase('test','1.0','TestDb',2*1024*1024);
    ```
1. transaction      根据情况控制事务提交或回滚
    ```
     db.transaction(function (context) {
            context.executeSql('CREATE TABLE IF NOT EXISTS testTable (id unique, name)');
            context.executeSql('INSERT INTO testTable (id, name) VALUES (0, "Byron")');
            context.executeSql('INSERT INTO testTable (id, name) VALUES (1, "Casper")');
            context.executeSql('INSERT INTO testTable (id, name) VALUES (2, "Frank")');
        });
    ```
1. executeSql       执行sql查询
    * 查询字符串
    * 用以替换查询字符串中问号的参数
    * 执行成功回调函数（可选）
    * 执行失败回调函数（可选）
    ```
    db.transaction(function (context) {
            context.executeSql('SELECT * FROM testTable', [], function (context, results) {
                var len = results.rows.length, i;
                console.log('Got '+len+' rows.');
                for (i = 0; i < len; i++){
                    console.log('id: '+results.rows.item(i).id);
                    console.log('name: '+results.rows.item(i).name);
                }
            });
        });
    ```