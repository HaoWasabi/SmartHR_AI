## TECH STACK CỤ THỂ
|**Layer.**|**Công nghệ**|**Lý do**|
|-------|--------|-----------------|
|Frontend|Next.js 15 (App Router) + TypeScript + TailwindCSS + shadcn/ui|Tốt cho form upload và hiển thị báo cáo|
|Auth|AWS Cognito|Tích hợp sẵn với API Gateway|
|API|API Gateway + Lambda (Python/Node.js)|Serverless|
|AI|Amazon Bedrock (Claude 3 Sonnet/ Kiro)|Mạnh về phân tích văn bản|
|RAG|Bedrock Knowledge Base + S3|Dễ triển khai|
|Storage|S3 (file CV) + DynamoDB (metadata & results)|Serverless|
|Document Parse|AWS Textract hoặc pdfplumber + python-docx|Trích xuất text|
|CI/CD|GitHub Actions → CodePipeline|Theo yêu cầu project|
|IaC|Terraform|Khuyến khích|
|Monitoring|Monitoring|-|