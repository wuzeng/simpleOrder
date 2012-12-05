# 数据库表结构设计


---
* [商品管理](#商品管理): product
* 


---
## 商品管理

* product

<table>
    <tr><th>列名</th><th>类型</th><th>说明</th><th>可空</th><th>默认值</th></tr>
    <tr><td>id</td><td>int(10)</td><td>标识列</td><td>非空</td><td></td></tr>
    <tr><td>name</td><td>varchar(60)</td><td>名称</td><td>非空</td><td></td></tr>
    <tr><td>type</td><td>varchar(30)</td><td>型号</td><td>非空</td><td></td></tr>
    <tr><td>sex</td><td>tinyint(4)</td><td>性别（1-男/2-女/3-中）</td><td>非空</td><td></td></tr>
    <tr><td>size</td><td>varchar(255)</td><td>尺码</td><td>非空</td><td></td></tr>
    <tr><td>image</td><td>varchar(255)</td><td>图片路径</td><td>可空</td><td>null</td></tr>
    <tr><td>price</td><td>decimal(10,2)</td><td>单价</td><td>非空</td><td>0.00</td></tr>
    <tr><td>visible</td><td>tinyint(4)</td><td>是否可见（0-可见/1-隐藏）</td><td>非空</td><td>0</td></tr>
    <tr><td>createtime</td><td>datetime</td><td></td><td>非空</td><td></td></tr>
    <tr><td>modifytime</td><td>datetime</td><td></td><td>非空</td><td></td></tr>
    <tr><td>status</td><td>tinyint(4)</td><td>状态（0-无效/1-有效）</td><td>非空</td><td>1</td></tr>
</table>