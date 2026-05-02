## DATABASE SCHEMA

**DynamoDB Tables** (khuyến nghị):

1. Table: Users

- PK: userId

- SK: profile

- Attributes: email, name, role (candidate/recruiter), createdAt

2. Table: Analyses

- PK: analysisId

- SK: userId

- Attributes:
    - cvFileKey (S3)
    - jdText
    - totalScore
    - categoryScores (JSON)
    - strengths (array)
    - weaknesses (array)
    - suggestions (array)
    - matchPercentage
    - createdAt
    - status (processing/completed/failed)


3. Table: JobDescriptions (cho 
RAG & lịch sử)

- PK: jdId

- Attributes: title, company, industry, rawText, embedding (nếu cần)