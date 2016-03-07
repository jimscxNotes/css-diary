## html5 �е�webSql
### �������ķ���
1. openDatabase     ʹ���������ݿ⣬�����Ǵ����µ����ݿ�
    �������������������:
    * ���ݿ�����
    * �汾
    * ��ʾ�����ݿ���
    * ���ݿ��С��
    * �ص����������Բ����ã�

    ```
    var db = openDatabase('test','1.0','TestDb',2*1024*1024);
    ```
1. transaction      ����������������ύ��ع�
    ```
     db.transaction(function (context) {
            context.executeSql('CREATE TABLE IF NOT EXISTS testTable (id unique, name)');
            context.executeSql('INSERT INTO testTable (id, name) VALUES (0, "Byron")');
            context.executeSql('INSERT INTO testTable (id, name) VALUES (1, "Casper")');
            context.executeSql('INSERT INTO testTable (id, name) VALUES (2, "Frank")');
        });
    ```
1. executeSql       ִ��sql��ѯ
    * ��ѯ�ַ���
    * �����滻��ѯ�ַ������ʺŵĲ���
    * ִ�гɹ��ص���������ѡ��
    * ִ��ʧ�ܻص���������ѡ��
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