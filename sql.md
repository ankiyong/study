```sql
SELECT DISTINCT 과목 FROM 성적;
SELECT 과목 FROM 성적 WHERE 학점 ='A';
SELECT DISTINCT 과목 FROM 성적 WHERE 학점 = 'A';
SELECT COUNT(DISTINCT 과목) FROM 성적;

[0-7]% 0~7로 시작하는 문자열
[^0-7]% 0~7로 시작하지 않는 문자열
```





```sql
SELECT price FROM product WHERE price BETWEEN 50000 AND 80000;
SELECT price FROM product WHERE price IN(40000,50000,70000);
SELECT price FROM product WHERE name LIKE '정보%';
SELECT * FROM product WHERE LIKE '[abcd]%';
SELECT price FROM product WHERE is NULL;
```

```sql
SELECT 학번,이름 FROM 학생 WHERE 학년 IN(3,4);
SELECT 이름 FROM 학생 WHERE 이름 LIKE '이%' ORDER BY 이름 DESC;
```

```sql
SELECT COUNT(직책), SUM(급여) FROM 급여 GROUP BY 직책;
SELECT SUM(급여) AS 급여합계 FROM 급여 GROUP BY 부서;
SELECT 직책,부서,SUM(급여) AS 급여합계 FROM 급여 GROUP BY 직책,부서;
SELECT COUNT(*) FROM 급여 
```

```sql
SELECT 직책,부서,SUM(급여) AS 급여합계 FROM 급여 GROUP BY 직책,부서 HAVING 급여합계 >= 5000;
```

```sql
SELECT 이름,과목,학점 FROM 성적 ORDER BY 학점 DESC,이름 ASC;
```

```sql
SELECT DISTINCT 전공 FROM 학생;
```

```sql
SELECT A.col1,A.col2,B.col1 FROM t1 A JOIN t2 B on 
```

```sql
SELECT A.책번호,A.책명,B.가격 FROM 도서 A JOIN 도서가격 B ON A.책번호 = B.책번호;
SELECT A.책번호,A.책명,B.가격 FROM 도서 A LEFT JOIN 도서가격 B;
SELECT A.책번호,A.책명,B.가격 FROM 도서 A RIGHT JOIN 도서가격 B ON A.책번호 = B.책번호;
SELECT A.책번호,A.책명,B.가격,B.책번호 FROM 도서 A FULL JOIN 도서가격 B ON A.책번호 = B.책번호;
SELECT A.책번호,A.책명,B.가격,B.책번호 FROM 도서 A CROSS JOIN 도서가격 B;
SELECT A.책번호,A.책명,B.가격,B.책번호 FROM 도서 A SELF JOIN 도서 B;
```

```sql
SELECT A.책번호,A.책병,B.가격 FROM 도서 A LEFT JOIN 도서가격 B ON A.책번호 = B.책번호;
```

```sql 
GRANT 권한 TO 사용자;
GRANT SELECT 권한 ON 테이블 TO 사용자;
GRANT SELECT 권한 ON 테이블 TO 사용자 WITH GRANT OPTION; - 특정 사용자에게 특정 테이블에 대한 권한을 부여하고 그 권한을 다른 사용자에게 부여할 수 있도록 함
```

```sql
REVOKE 권한 FROM 사용자;
REVOKE 권한 ON 테이블 FROM 사용자;
REVOKE 권한 ON 테이블 FROM 사용자 CASCADE CONSTRAINT; - 사용자에게 부여한 권한과 사용자가 부여한 권한 모두를 회수 
```

```sql
GRANT SELECT ON 사원 TO 홍길동;
```

