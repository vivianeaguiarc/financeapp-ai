# ER Diagram – FinanceApp-AI (Mermaid)

```mermaid
erDiagram
    Transaction {
        String id PK
        String name
        TransactionType type
        Decimal amount
        TransactionCategory category
        TransactionPaymentMethod paymentMethod
        DateTime date
        DateTime createdAt
        DateTime updatedAt
    }

    TransactionType {
        DEPOSIT
        EXPENSE
        INVESTMENT
    }

    TransactionCategory {
        HOUSING
        TRANSPORTATION
        FOOD
        ENTERTAINMENT
        HEALTH
        UTILITY
        SALARY
        EDUCATION
        OTHER
    }

    TransactionPaymentMethod {
        CREDIT_CARD
        DEBIT_CARD
        BANK_TRANSFER
        BANK_SLIP
        CASH
        PIX
        OTHER
    }

    Transaction ||--|| TransactionType : "has type"
    Transaction ||--|| TransactionCategory : "has category"
    Transaction ||--|| TransactionPaymentMethod : "has payment method"
```
