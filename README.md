# inflearn-jpa-study

인프런 **김영한의 자바 ORM 표준 JPA 프로그래밍 - 기본편** 학습 저장소입니다.

## 강의 / 학습 정보

- 강의: 자바 ORM 표준 JPA 프로그래밍 - 기본편 (김영한)
- 플랫폼: 인프런

## 사용 기술

- Java 11
- JPA / Hibernate (`hibernate-entitymanager`)
- JPQL
- MySQL (mysql-connector-j)
- Lombok
- Maven (`pom.xml`, 모듈별 빌드)

## 학습한 내용 (코드 근거)

### ex1-hello-jpa — JPA 기본과 엔티티 매핑
- 엔티티 매핑, 기본 키 전략 (`hellojpa/domain`)
- 연관관계 매핑: 단방향/양방향, 연관관계의 주인 (`Member`, `Team`, `MemberProduct`)
- 상속관계 매핑: `Item`-`Album`/`Book`/`Movie`, `@MappedSuperclass`(`BaseEntity`)
- 값 타입과 임베디드 타입: `Address`, `Period`, `AddressEntity`
- 영속성 전이(CASCADE)와 고아 객체: `Parent`-`Child`
- `RoleType` 등 enum 매핑

### hellojpa — JPQL
- JPQL 기본 문법과 쿼리 API (`jpql/JpaMain`)
- 프로젝션, DTO 조회 (`MemberDTO`)
- 커스텀 Dialect 예제 (`dialect/MySQLDialect`)

### jpashop — 실전 예제 도메인 모델
- 주문/상품/회원 도메인 설계: `Order`, `OrderItem`, `Item`(상속), `Member`, `Delivery`, `Category`
- 주문/배송 상태 enum: `OrderStatus`, `DeliveryStatus`
- (도메인 모델 매핑 중심으로 구성됨 — 기본편의 실전 예제 단계)

## 프로젝트 구조

```
inflearn-jpa-study/
├── ex1-hello-jpa/   # JPA 기본, 엔티티/연관관계/상속/값 타입 매핑
├── hellojpa/        # JPQL 문법과 쿼리 API
└── jpashop/         # 실전 예제 도메인 모델 설계
```
