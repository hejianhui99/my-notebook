总结：
###链接数据库
$conn = mysql_connect('主机名','用户名','密码')or die('链接失败');
判断数据库是否连接成功
if(!$conn){
	echo '链接失败';
}
连接数据库后就要设置数据库的编码
mysql_set_charset('utf8')
选择数据库
mysql_select_db('database_name')
操作数据库
	查
	存SQL语句
	获取数据的方式 3 种
	返回一条记录的索引数组
	mysql_fetch_row(query结果);
	返回一条记录的关联数组 （*常用*）
	mysql_fetch_assoc(result)
	返回一条记录的两种方式数组
	mysql_fetch_array(result)
	增
	修
	删
	执行SQL语句
	mysql_query();
	查询的次数
	mysql_num_rows();
	影响的次数
	mysql_affected_rows();
	释放结果
	mysql_free_result(result)

关闭数据库
mysql_close(链接数据库的资源);
