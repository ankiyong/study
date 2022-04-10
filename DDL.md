DDL

1. 개념 
   - 데이터를 정의하는 언어
2. 대상
   - 도메인,스키마,테이블,인덱스,뷰
3. 스키마
   - 외개내 - 외부스키마,개념스키마,내부스키마 
4. 테이블
   - 테이블/릴레이션, 컬럼/애트리뷰트, 로우/튜플, 식별자, 도메인, 차수, 카디널리티
5. 뷰

``` sql
CREATE VIEW view명 as select * from a;
CREATE OR REPLACE VIEW view명 as select * from a;
DROP VIEW view명;
```



6. 인덱스

- 순해비함 단결클 - 순서 인덱스, 해시 인덱스, 비트맵 인덱스, 함수기반 인덱스, 단일 인덱스, 결합 인덱스, 클러스터드 인덱스

7. 명령어

``` sql
CREATE [UNIQUE] INDEX 인덱스명 ON 테이블(컬럼);
ALTER [UNIQUE] INDEX 인덱스명 ON 테이블(컬럼);
DROP [UNIQUE] INDEX 인덱스명;
```



8. 인덱스 스캔 방식
   - 범전단생 - 인덱스 범위 스캔, 인덱스 전체 스캔, 인덱스 단일 스캔, 인덱스 생략 스캔