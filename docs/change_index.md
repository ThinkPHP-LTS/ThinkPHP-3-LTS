# 变更结构-索引表

1. 兼容PHP 7、PHP 8的变更：

   > String类修改为StringUtil类
   > 
   > 原因：String在php7中是保留字，不能用做类名
   > 
   > 位于：/Library/Org/Util/String.class.php
   > 
   > 变更后使用方法：原先 use Org\Util\String; 的地方，修改为 use Org\Util\StringUtil;

   > 参考：
   > https://blog.p2hp.com/archives/2800
   > https://blog.csdn.net/Lankecms/article/details/78090678
   > https://blog.csdn.net/weixin_35215045/article/details/116251737

2. 现代化Composer变更：

