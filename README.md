需求说明
========

目的
----

为老客户提供快捷下单订货渠道，方便对订单的管理，并提高客户满意度。

此版本特点
---------

* 为小用户群，低访问量。买家目前使用人数在100人以下，卖家一人一处登录。
* 功能简单，仅有下订单，无需线上支付。
* 此项目免费开源。

功能分析
-------

此项目包含两个部分：

### 前台
* 商品列表
* 订单详情
* 订单列表
* 个人信息

### 后台
* 商品管理
* 订单管理
* 字段管理

此项目有两个角色：
* 买家：拥有前台的浏览权限
* 卖家：拥有所有权限




前台——商品列表
-------------

* 展示实时数据，为客户提供购买参考
* 加入订单：有意向购买且有货商品加入订单，用户可以继续浏览，直到跳入订单详情页
* 向卖家提醒进货：有意向购买但无货商品

### 条件搜索
条件字段
* 名称：模糊查询
* 型号：模糊查询
* 性别：单选，input[type=radio]
* 尺码：多选，input[type=checkbox]，根据型号和性别联动而产生，例如：（型号=上衣;性别=男;尺码=[L,XL,XXL,XXXL]），（型号=长裤;性别=女;尺码=[25,26,27,28,29,30]）等
* 单价区间：单选+自定义，input[type=radio]，自定义部分为两个只可以填入自然数的input[type=text]

实现方式（待定）
* 联动部分：静态js或Ajax
* 查询动作：php或者Ajax更新到页面数据列表

### 排序功能
排序字段
* 名称
* 型号
* 单价

实现方式
* 用js event绑定在数据列表表头，点击触发排序，同时，会有箭头标识当前按照什么条件进行排序。
* 请求以及数据回显：Ajax

### 数据列表
数据表头
* 全选：input[type=checkbox]，选中之后，列表中所有的数据将被选中；取消选中操作，列表中所有数据将取消选中
* 图片
* 名称
* 型号
* 性别
* 尺码
* 单价

列表显示

特别说明


### 分页显示功能
### 订单功能

前台——订单详情
-------------
