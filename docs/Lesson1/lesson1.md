---
title: "Lesson1：お持ち帰りご注文用紙"
---
```mermaid

erDiagram
    orders ||--o{ product :""
    orders ||--o{ client :""
    product ||--|| category :""

    
  orders {
        int id PK "orderId"
        int clientId FK "顧客ID"
        int productId FK "商品ID"
        int amount
        int sum
        date orderDate
    }
  product {
        int id PK "商品ID"
        int categoryId FK "カテゴリID"
        string name
        number price
    }
  category {
        int id PK "カテゴリID"
        strig name
    }
  client {
        int id PK "顧客ID"
        string name
        number telephonenumber
    }
