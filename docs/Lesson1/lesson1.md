```mermaid

---
title: "属性定義"
---
erDiagram
    entity {
        type name PK "comment"
        type name FK "comment"
        type name UK
        type name "comment"
        type name
    }

erDiagram
    orders || -- o{	 client
    orders ||--o{  products