## KIẾN TRÚC DIAGRAM
```mermaid
flowchart TD
    subgraph Frontend
        UI[React/Next.js UI]
    end

    subgraph API
        APIGW[API Gateway]
        COG[Cognito Auth]
    end

    subgraph Backend
        LAMBDA[Lambda Functions]
        BEDROCK[Amazon Bedrock - Claude 3]
        KB[(Knowledge Base - RAG)]
    end

    subgraph Storage
        S3["S3 Bucket<br/>(CV files + JD)"]
        DYNAMO[(DynamoDB)]
    end

    UI --> APIGW
    APIGW --> COG
    APIGW --> LAMBDA
    LAMBDA --> BEDROCK
    LAMBDA --> S3
    LAMBDA --> KB
    LAMBDA --> DYNAMO
```

**Luồng chính:**

1. User upload CV → S3

2. Lambda trigger → Extract text (Textract hoặc PDF parser)

3. Gọi Bedrock với Prompt Engineering + RAG

4. Lưu kết quả vào DynamoDB

5. Trả báo cáo về Frontend
