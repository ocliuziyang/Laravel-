#Laravel实现微信树洞效果
####链接参数分析
```
*http://www.jingl520.com/mobile/reply?ac=listshit&topicId=2027&orderBy=2&wxaccount=gh_b315c2abe8ce&userwx=owRT7jvBXKfqEiUaFOIqnlNWL6yo&aId=274*
//当然域名不能忘,这使用的是get方式请求树洞留言列表的方式
//&符号用来分割参数
//下面让我们来分析参数
1.ac=listshit->这是路由动作
2.topicId=2027->这是留言id
3.orderBy=2->排序方式(热门,最新,推荐)
4.wxaccount=gh_b315c2abe8ce->微信公众号id
5.userwx=owRT7jvBXKfqEiUaFOIqnlNWL6yo->用户的微信id
6.aId=274->未知
```
####数据库treeholes表设计
|	字段名	|	数据类型	|	自增长	|默认值| 备注 |
|	:-----	|:-------		|	:----	|:----| :------|
| id	|	integer	|	是		|		|留言显示id|
|content	|	string	|	否		|		|留言|
|content_bgcolor	|	string	|	否		|		|留言icon颜色|
|view	|	integer	| 		否	|		| 浏览次数 |
|published_time	|	time	| 		---	|		| 发布时间 |
####页面
>1.留言列表页
	
>2.



##最后附上github连接 [gitHub链接](http://github.com/ocliuziyang)

