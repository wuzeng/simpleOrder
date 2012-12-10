# 数据库表结构设计
---

* [商品管理](#商品管理): product
* [订单管理](#订单管理): order
* [订单详情](#订单详情): detail
* [提醒进货](#提醒进货): purchase
* [界面语言](#界面语言): language
* [尺码管理](#尺码管理): size


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

[回顶部](#数据库表结构设计)

---
## 订单管理

* order

<table>
    <tr><th>列名</th><th>类型</th><th>说明</th><th>可空</th><th>默认值</th></tr>
    <tr><td>id</td><td>int(10)</td><td>标识列</td><td>非空</td><td></td></tr>
    <tr><td>name</td><td>varchar(60)</td><td>姓名</td><td>非空</td><td></td></tr>
    <tr><td>phone</td><td>varchar(30)</td><td>电话</td><td>非空</td><td></td></tr>
    <tr><td>deliverdate</td><td>date</td><td>交货日期</td><td>非空</td><td></td></tr>
    <tr><td>deliveraddress</td><td>varchar(255)</td><td>交货地点</td><td>非空</td><td></td></tr>
    <tr><td>totalmoney</td><td>decimal(10,2)</td><td>总金额</td><td>非空</td><td></td></tr>
    <tr><td>subscription</td><td>decimal(10,2)</td><td>订金</td><td>非空</td><td></td></tr>
    <tr><td>payment</td><td>varchar(30)</td><td>支付方式</td><td>非空</td><td></td></tr>
    <tr><td>email</td><td>varchar(60)</td><td>电子邮箱</td><td>非空</td><td></td></tr>
    <tr><td>step</td><td>tinyint(4)</td><td>处理情况（0-未处理/1-已处理）</td><td>非空</td><td></td></tr>
    <tr><td>createtime</td><td>datetime</td><td></td><td>非空</td><td></td></tr>
    <tr><td>modifytime</td><td>datetime</td><td></td><td>非空</td><td></td></tr>
    <tr><td>status</td><td>tinyint(4)</td><td>状态（0-无效/1-有效）</td><td>非空</td><td>1</td></tr>
</table>

[回顶部](#数据库表结构设计)

---
## 订单详情

* detail

<table>
    <tr><th>列名</th><th>类型</th><th>说明</th><th>可空</th><th>默认值</th></tr>
    <tr><td>id</td><td>int(10)</td><td>标识列</td><td>非空</td><td></td></tr>
    <tr><td>orderid</td><td>int(10)</td><td>订单主表id</td><td>非空</td><td></td></tr>
    <tr><td>productid</td><td>int(10)</td><td>商品主表id</td><td>非空</td><td></td></tr>
    <tr><td>size</td><td>varchar(20)</td><td>尺码</td><td>非空</td><td></td></tr>
    <tr><td>count</td><td>int(10)</td><td>购买数量</td><td>非空</td><td></td></tr>
    <tr><td>totalmoney</td><td>decimal(10,2)</td><td>总金额</td><td>非空</td><td></td></tr>
    <tr><td>createtime</td><td>datetime</td><td></td><td>非空</td><td></td></tr>
    <tr><td>modifytime</td><td>datetime</td><td></td><td>非空</td><td></td></tr>
    <tr><td>status</td><td>tinyint(4)</td><td>状态（0-无效/1-有效）</td><td>非空</td><td>1</td></tr>
</table>

[回顶部](#数据库表结构设计)

---
## 提醒进货

* purchase

<table>
    <tr><th>列名</th><th>类型</th><th>说明</th><th>可空</th><th>默认值</th></tr>
    <tr><td>id</td><td>int(10)</td><td>标识列</td><td>非空</td><td></td></tr>
    <tr><td>productid</td><td>int(10)</td><td>商品主表id</td><td>非空</td><td></td></tr>
    <tr><td>size</td><td>varchar(20)</td><td>尺码</td><td>非空</td><td></td></tr>
    <tr><td>step</td><td>tinyint(4)</td><td>处理情况（0-未处理/1-已处理）</td><td>非空</td><td></td></tr>
    <tr><td>createtime</td><td>datetime</td><td></td><td>非空</td><td></td></tr>
    <tr><td>modifytime</td><td>datetime</td><td></td><td>非空</td><td></td></tr>
    <tr><td>status</td><td>tinyint(4)</td><td>状态（0-无效/1-有效）</td><td>非空</td><td>1</td></tr>
</table>

[回顶部](#数据库表结构设计)

---
## 界面语言

* language

<table>
    <tr><th>列名</th><th>类型</th><th>说明</th><th>可空</th><th>默认值</th></tr>
    <tr><td>id</td><td>int(10)</td><td>标识列</td><td>非空</td><td></td></tr>
    <tr><td>en</td><td>varchar(255)</td><td>英语</td><td>非空</td><td></td></tr>
    <tr><td>cn</td><td>varchar(255)</td><td>汉语</td><td>非空</td><td></td></tr>
    <tr><td>rus</td><td>varchar(255)</td><td>俄语</td><td>非空</td><td></td></tr>
    <tr><td>createtime</td><td>datetime</td><td></td><td>非空</td><td></td></tr>
    <tr><td>modifytime</td><td>datetime</td><td></td><td>非空</td><td></td></tr>
    <tr><td>status</td><td>tinyint(4)</td><td>状态（0-无效/1-有效）</td><td>非空</td><td>1</td></tr>
</table>

[回顶部](#数据库表结构设计)

---
## 尺码管理

* size

<table>
    <tr><th>列名</th><th>类型</th><th>说明</th><th>可空</th><th>默认值</th></tr>
    <tr><td>id</td><td>int(10)</td><td>标识列</td><td>非空</td><td></td></tr>
    <tr><td>type</td><td>varchar(30)</td><td>型号</td><td>非空</td><td></td></tr>
    <tr><td>sex</td><td>tinyint(4)</td><td>性别（1-男/2-女/3-中）</td><td>非空</td><td></td></tr>
    <tr><td>size</td><td>varchar(255)</td><td>尺码</td><td>非空</td><td></td></tr>
    <tr><td>createtime</td><td>datetime</td><td></td><td>非空</td><td></td></tr>
    <tr><td>modifytime</td><td>datetime</td><td></td><td>非空</td><td></td></tr>
    <tr><td>status</td><td>tinyint(4)</td><td>状态（0-无效/1-有效）</td><td>非空</td><td>1</td></tr>
</table>

[回顶部](#数据库表结构设计)
