Here's the table with IAM usernames with the first two letters capitalized:

## S3 Bucket - 1 Full Access and 2 Read Only

| IAM User Name | Full Name | Role | Access Level | Justification |
|---------------|-----------|------|--------------|---------------|
| BScott | Benjamin Scott | Cloud Engineer | Full Access | Storage admin duties: create buckets, manage lifecycle/replication/encryption, and handle data pipelines and backups---requires full S3 control. |
| DRodriguez | Daniel Rodriguez | Network Officer | Read Only | Network ops often review logs/config snapshots and static assets stored in S3; read-only prevents unintended changes while enabling investigation. |
| JCampbell | Jessica Campbell | Network Officer | Read Only | Same rationale as above: access to bucket contents for diagnostics and reviews without the risk of writes or policy edits. |

## Machine Learning - 2 Full Access

| IAM User Name | Full Name | Role | Access Level | Justification |
|---------------|-----------|------|--------------|---------------|
| SMorales | Sophia Morales | AI Specialist | Full Access | Needs to build/train/deploy models, manage notebooks, jobs, endpoints, and pipelines; full ML access is essential for end-to-end AI workflows. |
| MGrant | Matthew Grant | AI Specialist | Full Access | Needs to build/train/deploy models, manage notebooks, jobs, endpoints, and pipelines; full ML access is essential for end-to-end AI workflows. |

## EC2 - 1 Full Access and 2 Read Only

| IAM User Name | Full Name | Role | Access Level | Justification |
|---------------|-----------|------|--------------|---------------|
| MBennett | Marcus Bennett | Senior Cloud Engineer | Full Access | Primary infra owner: must create/modify instances, ASGs, ALBs, security groups, and AMIs; full access aligns with senior ownership and change responsibility. |
| ETurner | Emily Turner | Senior Network Specialist | Read Only | Needs visibility into instances, security groups, routes, and ENIs for troubleshooting and audits; no day-to-day need to mutate compute---least privilege fits. |
| OCarter | Olivia Carter | Cloud Engineer | Read Only | Handles monitoring and triage; read access is sufficient for reviews, while change control remains with the senior engineer. |