# How to View the ER Diagram

The Mermaid `erDiagram` syntax may not render properly on this site due to limitations of the current Mermaid version.

To view the ER diagram correctly, follow these steps:

---

## 📤 Steps to View in Mermaid Live Editor

1. Open the [Mermaid Live Editor](https://mermaid.live/edit).
2. Copy the content below and paste it into the left-hand editor panel.
3. Click the **"Full screen"** button in the top-right to expand the diagram.

---

## 📋 Diagram Code (copy this)

````mermaid
erDiagram
    USERS ||--o{ ORDERS : places
    USERS {
        id bigint PK
        name varchar(45)
        email string
    }
    ORDERS {
        id int PK
        user_id int FK
        order_date date
    }
```
