# 장바구니 미션 (협업)

## 💋 회의 일정

- [23.05.26 회의 내용](https://deciduous-buffalo-838.notion.site/091f083751e1486c99356e8d5c46c009)

## 💋 결정된 내용

- 2단계 선택 요구사항: 포인트로 결정

## 💋 추가적으로 회의가 필요한 내용

- 사용자별 주문 목록 조회
- 주문 상세 정보 조회


## 💋 결제 시나리오
1. 구매할 상품 조회 
2. 사용자 포인트 조회
3. 포인트 사용 금액 결정
4. 결제


## 💋 API 명세

### `GET users/points`

#### Request

Header

```yaml
{
    "Authorization": Basic ${credentials}
}
```

#### Response

Body
        
```json
{
    "points": 123 
}
```

### `POST /cart-items/payment`

#### Request

Header

```yaml
{
    "Authorization": Basic ${credentials}
}
```

Body

```json
{
    "cartItemIds": [
        {
            "cartItemId": 1 
        },
        {
            "cartItemId": 3
        }
    ]
    "points": 100,
}
```
        
#### Response

```
201 CREATED  /orders/histories/1
```
