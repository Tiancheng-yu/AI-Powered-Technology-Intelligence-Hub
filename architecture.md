# AI-Powered Technology Intelligence Hub

```mermaid
flowchart TD

A[RSS Sources]

A --> A1[OpenAI]
A --> A2[Anthropic]
A --> A3[Microsoft Security]
A --> A4[Microsoft 365]
A --> A5[AWS Security]
A --> A6[The Hacker News]
A --> A7[ITPro]

A1 --> B
A2 --> B
A3 --> B
A4 --> B
A5 --> B
A6 --> B
A7 --> B

B[n8n Automation Platform<br/>Docker Self-Hosted]

B --> C[RSS Feed Aggregation]

C --> D[Category Classification]

D --> E[RSS Deduplication]

E --> F[Load Existing Notion Links]

F --> G[Duplicate Validation]

G --> H{Already Exists?}

H -->|Yes| I[Skip Article]

H -->|No| J[Clean Content]

J --> K[AI Summarisation<br/>OpenAI API]

K --> L[Create Notion Record]

L --> M[Technology Intelligence Hub]

M --> N[Search & Review]
     
```