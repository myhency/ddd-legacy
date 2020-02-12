# 키친포스

## 요구 사항

치킨집의 포스기계에서 사용하는 어플리케이션을 구현한다.

### 메뉴그룹(MenuGroup)

- [ ] 메뉴가 제공되는 형태를 메뉴그룹이라고 부른다.
- [ ] 메뉴그룹을 설정할 수 있다.
- [ ] 메뉴그룹 목록을 볼 수 있다.

### 메뉴(Menus)

- [ ] 고객에게 제공되는 음식을 메뉴라고 부른다.
- [ ] 메뉴를 생성할 수 있다.
    - [ ] 메뉴를 생성할 때 메뉴의 가격을 반드시 입력해야 한다.    
    - [ ] 메뉴의 가격이 올바르지 않으면 등록할 수 없다.
        - [ ] 메뉴의 가격은 0 원 이상이어야 한다.
        - [ ] 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- [ ] 각 메뉴는 반드시 하나 이상의 메뉴그룹에 속한다.
- [ ] 메뉴 목록을 볼 수 있다.

### 주문(Orders)

- [ ] 테이블에 서빙되는 메뉴의 집합을 주문이라고 부른다.
- [ ] 주문을 생성할 수 있다.
    - [ ] 주문메뉴가 반드시 있어야 한다.
    - [ ] 매장에서 판매하지 않는 메뉴를 주문할 수 없다.
    - [ ] 주문할 때 테이블을 반드시 지정해야 한다.
    - [ ] 주문이 들어오면 주문상태가 조리중(COOKING)으로 된다.
- [ ] 주문 목록을 볼 수 있다.
- [ ] 주문의 상태를 변경할 수 있다.
(조리중: COOKING, 고객이 식사중인 주문: MEAL, 식사가 끝나고 결재도 끝난 주문: COMPLETION)
    - [ ] 이미 생성된 주문의 상태만 변경할 수 있다.
    - [ ] 식사가 끝나고 결재도 끝난 주문은 상태를 변경할 수 없다.

### 상품(Products)

- [ ] 치킨집에서 제공할 수 있는 음식의 종류이다.
- [ ] 상품을 생성할 수 있다.
    - [ ] 상품을 생성할 때 상품의 가격을 반드시 입력해야 한다.
    - [ ] 상품을 생성할 때 상품의 가격은 반드시 양수를 입력해야 한다.
- [ ] 상품 목록을 볼 수 있다.

### 테이블(Tables)

- [ ] 고객이 식사를 하는 자리를 테이블이라고 부른다.
- [ ] 테이블 정보를 입력할 수 있다. (단체석, 손님 수, 테이블상태(비었는지 아닌지))
- [ ] 테이블상태를 변경할 수 있다.
    - [ ] 주문이 없는 테이블의 상태를 변경할 수 없다.
    - [ ] 단체석에 포함되지 않은 테이블은 변경할 수 없다.
    - [ ] 조리중이거나 손님이 식사중인 테이블의 상태를 변경할 수 없다.
- [ ] 테이블에 손님수를 변경할 수 있다.
    - [ ] 손님수는 반드시 양수여야 한다.
    - [ ] 주문이 있는 테이블의 손님수만 변경할 수 있다.
- [ ] 테이블 목록을 볼 수 있다.

### 단체석(TableGroup)

- [ ] 한 개 이상의 테이블이 붙어 있는 것(물리적 또는 논리적으로)을 단체석이라고 부른다.
(예를 들어 물리적으로 떨어져 있는 테이블이나 손님들이 같은 일행일 경우)
- [ ] 단체석을 생성할 수 있다.
    - [ ] 주문이 없는 테이블은 단체석으로 생성할 수 없다.
    - [ ] 주문이 있는 경우에도 두개 이상의 테이블만 단체석으로 생성할 수 있다.
    - [ ] 주문이 있는 테이블수와 생성하려는 테이블수가 같아야 한다.
    - [ ] 단체석을 생성하는 대상 테이블은 비어있어야 한다.
- [ ] 단체석을 비울 수 있다.
    - [ ] 테이블상태가 조리중: COOKING, 고객이 식사중인 주문: MEAL 인 경우는 비울 수 없다.

## 용어 사전

| 한글명 | 영문명 | 설명 |
| --- | --- | --- |
|  |  |  |

## 모델링

## 기타

![legacypos 테이블 관계도](assets/legacypos_tables.jpg)
