### �������
1. ʹ��div�ձ�ǩ���������������ǿ鼶Ԫ�أ�����display��block��
    ```
    .clear{clear:both}
    <div class=��clearfix��>
        <div class=��left��>�����󸡶�</div>
        <div class=��right��>�����Ҹ���</div>
        <div class=��clear��></div>
    </div>
    ```
1. ��Ԫ������ overflow��hidden��
1. ����div���� α��:after �� zoom
    ```
    .clearfix:after {content:��\200B��; display:block; height:0; clear:both; }
    .clearfix { *zoom:1; } �չ�IE6��IE7�Ϳ�����
    ```