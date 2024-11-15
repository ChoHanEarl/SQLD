# Chapter 1 데이터 모델링의 이해
## 1장 데이터 모델링의 이해
### 1절 데이터 모델의 이해

- 데이터 모델링이란?
1. 정보시스템을 구축하기 위한 데이터 관점의 업무 분석 기법
2. 현실 세계의 데이터를 약속된 표기법으로 표현하는 과정
3. 데이터베이스 구축을 위한 분석 및 설계의 과정

- 데이터 모델링의 특징: 추상화, 단순화, 명확성

- 관점: 데이터, 프로세스(업무), 상관(처리 방식)

- 유의사항: 유연성, 유일성, 일관성

- 데이터 모델링의 3단계:
1. 개념적(추상)
2. 논리적(정규화)
3. 물리적(DB)

- 데이터베이스 스키마 구조: 외부(뷰), 개념(통합된 사용자), 내부(물리)

- 데이터 독립성: 논리적 독립성, 물리적 독립성

- 데이터 모델링의 3요소: 엔티티(Entity), 관계, 속성

- ERD 작성 순서:
1. 엔티티 도출
2. 배치
3. 관계 설정
4. 관계명 기술
5. 관계 차수 설정
6. 선택사양 기술

### 2절 엔티티(Entity)
- 엔티티의 정의: 업무에서 관리해야 하는 데이터의 집합, 단수명사, 인스턴스의 집합

- 특징:
1. 업무에서 필요로 함
2. 유일한 식별자
3. 2개 이상의 인스턴스 집합
4. 업무 프로세스에서 이용됨
5. 2개 이상의 속성
6. 관계 가짐

- 엔티티의 분류
1. 유무형에 따른 분류: 유형 엔티티, 무형 엔티티
2. 발생 시점에 따른 분류: 기본 엔티티, 중심 엔티티, 행위 엔티티

- 엔티티 명명 규칙:
1. 협업에서 사용되는 용어
2. 약어 사용 지양
3. 단수 명사
4. 유일성 보장
5. 의미 명확

### 3절 속성(Property)
- 정의: 업무에서 필요로 하는 인스턴스에서 관리하고자 하는, 의미상 더 분리되지 않는 최소의 데이터 단위

- 특징:
1. 업무에서 필요
2. 주식별자에 함수적으로 종속(PK 변경되면 속성도 변경)
3. 1개의 속성은 1개의 속성값 가짐
4. 속성도 집합

- 특성에 따른 분류: 기본 / 설계 / 파생 속성

- 분해 가능 여부: 단일 / 복합 / 단일값 / 다중값 속성

- 도메인: 속성이 가질 수 있는 값의 범위

### 4절 관계
- 관계의 표기법: 관계명, 관계차수(多는 삼발 표시), 관계 선택사양(필수는 I, 선택은 O로 표시)

- ERD: 존재관계, 행위관계 (표기 구분 안 함)

- UML: 연관관계(실선, 멤버변수), 의존관계(점선, 파라미터)

| 식별관계(실선) | 비식별관계(점선) |
|---------------|-----------------|
| 강한 연결관계 | 약한 연결관계 |
| 자식 식별자의 구성에 포함 | 자식 일반 속성에 포함 |
| 부모 엔터티에 종속 |              |

### 5절 식별자
- 정의: 엔티티를 대표할 수 있는 유일성을 만족하는 속성 (자주 이용되는 속성, 명칭이나 내역 이름은 X)

- 특징: 유일성 / 최소성 / 불변성 / 존재성

| **대표성** | 주식별자 | 보조식별자 |
|------------|---------|-----------|
| **스스로 생성** | 내부식별자 | 외부식별자 |
| **속성의 수** | 단일식별자 | 복합식별자 |
| **대체 여부** | 본질식별자 | 인조식별자 |

