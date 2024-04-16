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
只能出现集函数和分组属性，上述只能

