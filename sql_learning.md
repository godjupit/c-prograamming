# SQL查询
## 对查询结果进行排序
ASC 表示升序

DESC表示降序                 
ORDER BY ___ DESC;      
  ## 使用集函数
  COUNT(*)  
  SUM()  
  AVG()   
  MAX()  
  MIN()  

  查询学生总人数  
      
        
```
SELECT count(distinct Sno)
FROM student
```
查询选修一号课程的学生考试成绩平均值
```
SELECT count(distinct Sno)
FROM student
```
_注意_  用DISTINCT避免学生人数重复计算  
  
查询非空数值
```sql
SELECT *
FROM student
WHERE sno IS NOT NULL;
```  
## 通配符
  
  ## 分组
```sql
SELECT Cno， COUNT(Sno)
FROM SC
GROUP BY Cno;
```  
分组方法：按照指定一列或多列值分组  
只能出现集函数和分组属性 意味着只能出现两行
```sql
count(*) 计算查询结果有多少行
SELECT  Sno,  COUNT(*)   查询结果只包含集函数和查询列
FROM   SC
WHERE Grade>=90
GROUP BY Sno            按照序号进行分组，同时查询每个组有多少行，*不能避免空值，如果不要查询空值需要用具体列
HAVING COUNT(*)>=3；    相当于where 每个组的数量需要大于3


