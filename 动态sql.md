
# 动态SQL
### if
动态SQL通常要做的事情是根据条件包含where子句的一部分，比如：
```
<select id="findActiveBlogWithTitleLike"
resultType="Blog">
select * from blog
where state="active"
<if test="title!=null">
and title like #{title}
</if>
</select>
```
这条语句提供了一种可选的查找文本功能。如果没有传入“title”，那么所有处于“active”状态的BLOG
