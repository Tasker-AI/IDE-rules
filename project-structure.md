# Project Structure

This file describes the high-level directory layout and the purpose of each main folder.  
Keep this up-to-date whenever significant structural changes are introduced so that new collaborators and automations can navigate the codebase quickly.

## Tech Stack (This is just an example, and should be updated by the Project architecture assistant)
- Lambda Backend
- CloudWatch lambda logs
- React Frontend
- Tailwind CSS
- CDK Infrastructure / Deployment
- Cognito Authentication
- IAM Roles
- SSM Parameter Store
- AWS Secrets Manager
- DynamoDB
- S3 Execution Logs

## Root-level layout (This is just an example, and should be updated by the Project architecture assistant)

| Path | Purpose |
|------|---------|
| `backend/` | Source code for all backend services. |
| `frontend/` | All front-end applications. |
| `infrastructure/` | Cloudformation describing cloud resources, networking, and CI/CD pipelines. |

## Backend structure and conventions (This is just an example, and should be updated by the Project architecture assistant)
* Example convention
* Example convention 2

```
backend/
├── lambdas/                                    
│   ├── adapter/
│   ├── common/python/common                    # Shared Python helper modules (Lambda layer)
│   ├── main-lambda-service/
│   │   ├── adapters/
│   │   │   └── operations/
│   │   ├── admin/
│   │   │   └── operations/
└── requirements.txt                            # Shared Python deps for Lambda layer
```


## Frontend structure and conventions (This is just an example, and should be updated by the Project architecture assistant)
* Example convention
* Example convention 2

```
frontend/
└── app-name/
    ├── public/                       # Static assets served by CRA
    ├── src/
    │   ├── adapters/                 # API adapters
    │   ├── assets/                   # Images, fonts, etc.
    │   ├── components/               # Shared React components
    │   ├── config/                   # Front-end configuration helpers
    │   ├── contexts/                 # React context providers
    │   ├── hooks/                    # Custom hooks (useFoo)
    │   ├── lib/                      # Non-React TS utilities
    │   ├── prompts/                  # LLM prompt templates
    │   ├── services/                 # Business-layer services
    │   ├── types/                    # Global TypeScript types
    │   └── utils/                    # Helper functions
    ├── tests/                        # React Testing Library + Vitest tests
    ├── tailwind.config.js            # Tailwind CSS config
    ├── tsconfig.json                 # TypeScript compiler options
    └── package.json
```


## Infrastructure structure and conventions (This is just an example, and should be updated by the Project architecture assistant)
* Example convention
* Example convention 2

```
infrastructure/
├── app.py                              # CDK entry point
├── cdk.json                            # CDK CLI configuration
├── example/                            # Python CDK stacks & constructs
│   ├── __init__.py
│   └── example.py
├── files/                              # Static JSON assets deployed with stacks
└── logs/                               # Synth/deploy logs (git-ignored)
```

## Database Schema
- Example csvs of the database tables can be found in `local-test\database_tables\`
- Table name 1
- Table name 2
- Table name 3