---
title: "Lesson2：図書館の予約申込書"
---

```mermaid

erDiagram
    Request ||--|| Client :""
    Request ||--|| Book :""
    Client ||--|{ ContactOption :""

  Request {
        int id PK
        int client id FK
        int book_id FK
        int requested_date
        timestamp created_at
        timestamp updated_at
    }

  Client {
        int id PK "顧客ID"
        string name
        enum contact_option FK
        int telephone_number
        boolean notify_family
        string location
        string how_to_know_book
        timestamp created_at
        timestamp updated_at
    }

  ContactOption {
        int id PK
        int (HOME/TELL_PHONE/FAX/COMPANY_TELL)
        timestamp created_at
        timestamp updated_at
    }


  Book {
        int id PK "書籍ID"
        string name
        string author
        string publish_company
        string publish_at
        int cost
        timestamp created_at
        timestamp updated_at
    }
```
