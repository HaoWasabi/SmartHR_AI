# SmartHR_AI
 SmartHR AI - Hệ thống chấm điểm CV thông minh bằng AWS Bedrock.

**Mô tả:** Ứng dụng web cho phép candidate upload CV và Job Description để nhận điểm số chi tiết, phân tích mạnh/yếu và gợi ý cải thiện. Sử dụng RAG để so sánh với tiêu chuẩn ngành.

## Tính năng nổi bật

- Chấm điểm CV theo Job Description với độ chính xác cao
- Phân tích chi tiết + gợi ý cải thiện cụ thể
- Hỗ trợ RAG (kiến thức ngành)
- ATS Friendly Score
- Export báo cáo PDF

## Tech Stack

- **Frontend**: Next.js 15, TypeScript, TailwindCSS, shadcn/ui
- **Backend**: AWS Lambda, API Gateway
- **AI**: Amazon Bedrock (Claude 3 Sonnet/Kiro)
- **Auth**: AWS Cognito
- **Storage**: S3 + DynamoDB
- **IaC**: Terraform
- **CI/CD**: GitHub Actions + AWS CodePipeline

## Kiến trúc

[Xem thêm tại đây](docs/ARCHITECTURE.md)

## Prerequisites

- AWS Account
- Terraform >= 1.5
- Node.js 20+
- AWS CLI configured

## Triển khai

```bash
# 1. Infrastructure
cd infra
terraform init
terraform apply

# 2. Frontend
cd frontend
npm install
npm run dev
```

## Project Structure
```
SmartHR_AI/
├── frontend/          # Next.js app
├── backend/lambda/    # Lambda functions
├── infra/             # Terraform IaC
├── docs/              # Tài liệu
└── prompts/           # Prompt templates
```

## Demo & Screenshots
*(Bổ sung sau)*