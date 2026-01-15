# AIExperiments
# Document Management System -- Jira Stories with Sub-Tasks

This README captures Jira Epics, Stories, and role-based sub-tasks for a
3‑month delivery of a Document Management System supporting onboarding
with OCR and AI-assisted prefill.

------------------------------------------------------------------------

## Story 1.1.1 -- Customer uploads documents before application

### Architecture

-   Define entity-centric document domain model
-   Define document lifecycle independent of application lifecycle

### Design

-   Design pre-application upload user experience
-   Design upload progress and status indicators

### AWS Implementation

-   Design S3 bucket strategy with entity-level prefixes
-   Implement pre-signed URL upload mechanism

### Business Analysis

-   Define pre-application eligibility rules
-   Define success metrics for data prefill

### Development

-   Implement upload UI
-   Implement backend upload APIs

### Testing

-   Test upload before application creation
-   Test invalid file scenarios

### DevOps

-   Setup CI/CD pipelines
-   Configure IAM roles and secrets

### SRE

-   Define upload SLIs/SLOs
-   Configure alerting on upload failures

------------------------------------------------------------------------

## Story 1.1.2 -- RM uploads documents at entity level

### Architecture

-   Extend entity document model for RM role
-   Define role-based document permissions

### Design

-   Design RM entity document grid
-   Design document reuse indicators

### AWS Implementation

-   Configure Cognito role mapping
-   Enforce IAM-based access control

### Business Analysis

-   Document RM onboarding workflows
-   Define reuse constraints

### Development

-   Implement RM upload screens
-   Implement reuse linking logic

### Testing

-   Test role-based access
-   Test cross-journey reuse

### DevOps

-   Feature flag RM flows

### SRE

-   Monitor RM upload volumes
