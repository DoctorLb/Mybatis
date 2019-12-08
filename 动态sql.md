
#动态SQL
###if
动态SQL通常要做的事情是根据条件包含where子句的一部分，比如：
```
<select id="findActiveBlogWithTitleLike"
resultType="Blog">
select * from blog
where state="active"


```
