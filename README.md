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

EPIC 1: Entity-Centric Document Repository & Pre-Application Upload

Outcome: Enable early document capture and reuse across onboarding journeys.

Feature 1.1: Entity-Level Document Storage
	•	Story 1.1.1 (Customer | High)
As a Customer, I want to upload documents before starting my application so that my information can be reused later.
	•	Story 1.1.2 (RM | High)
As a Relationship Manager, I want to upload documents directly against an entity so that documents can be reused across journeys.
	•	Story 1.1.3 (Ops | Medium)
As an Operations user, I want to view all documents associated with an entity across journeys so that I can validate completeness.

Feature 1.2: Document Reuse Across Journeys
	•	Story 1.2.1 (RM | High)
As an RM, I want to reuse documents uploaded in previous journeys to avoid re-requesting documents.
	•	Story 1.2.2 (Ops | Medium)
As Ops, I want reused documents to retain original metadata and audit history.

⸻

EPIC 2: Multi-Channel Document Upload & Bulk Handling

Outcome: Make document intake fast and flexible for all users.

Feature 2.1: Multiple Upload Methods
	•	Story 2.1.1 (Customer | High)
As a Customer, I want to upload documents using drag-and-drop or file selection so that uploading is easy.
	•	Story 2.1.2 (RM | High)
As an RM, I want to upload multiple documents at once so that I save time.

Feature 2.2: Bulk Upload & Apply-to-All
	•	Story 2.2.1 (RM | High)
As an RM, I want to bulk upload documents and apply the same metadata to all so that onboarding is faster.
	•	Story 2.2.2 (Ops | Medium)
As Ops, I want bulk uploads to respect document type and access rules.

⸻

EPIC 3: Document Metadata, Classification & Access Control

Outcome: Ensure documents are structured, secure, and discoverable.

Feature 3.1: Document Metadata Capture
	•	Story 3.1.1 (Customer | High)
As a Customer, I want document names and types to be auto-suggested so that I don’t make mistakes.
	•	Story 3.1.2 (RM | High)
As an RM, I want to edit document metadata so that documents are correctly classified.

Feature 3.2: Access Layers & Permissions
	•	Story 3.2.1 (Ops | High)
As Ops, I want business and geographic access controls so that sensitive documents are only visible to authorised users.
	•	Story 3.2.2 (Ops | Medium)
As Ops, I want access restrictions to be enforced automatically based on policy.

⸻

EPIC 4: Document Requirement Lifecycle Management

Outcome: Track, control, and complete document requirements reliably.

Feature 4.1: Requirement Status Management
	•	Story 4.1.1 (Ops | High)
As Ops, I want document requirements to move automatically to approval pending when a document is uploaded.
	•	Story 4.1.2 (Ops | High)
As Ops, I want to approve or reject document submissions to maintain compliance.

Feature 4.2: Waive & Defer Workflows
	•	Story 4.2.1 (Ops | Medium)
As Ops, I want to defer document requirements with a future date so onboarding can progress.
	•	Story 4.2.2 (Ops | Medium)
As Ops, I want to waive document requirements with justification so that exceptions are auditable.

Feature 4.3: Bulk Status Updates
	•	Story 4.3.1 (Ops | Medium)
As Ops, I want to update the status of multiple requirements at once so that I save time.

⸻

EPIC 5: OCR & AI-Driven Data Extraction and Pre-Fill

Outcome: Reduce manual data entry and accelerate onboarding.

Feature 5.1: OCR & Text Extraction
	•	Story 5.1.1 (System | High)
As the system, I want to extract text from uploaded documents so that data can be reused.
	•	Story 5.1.2 (Ops | High)
As Ops, I want to see extracted text linked to the source document for verification.

Feature 5.2: AI-Based Classification & Field Extraction
	•	Story 5.2.1 (System | High)
As the system, I want to classify document types automatically to reduce manual tagging.
	•	Story 5.2.2 (System | High)
As the system, I want to extract key fields (e.g., name, address, registration number) to pre-fill applications.

Feature 5.3: Human Review & Approval of Extracted Data
	•	Story 5.3.1 (Ops | High)
As Ops, I want to review and approve extracted data before it is written to the application.
	•	Story 5.3.2 (Ops | Medium)
As Ops, I want to override incorrect AI-extracted values with an audit trail.

⸻

EPIC 6: Error Handling, Validation & Auditability

Outcome: Ensure resilience, trust, and regulatory readiness.

Feature 6.1: Upload Validation & Failure Handling
	•	Story 6.1.1 (All Users | High)
As a user, I want clear error messages when a document upload fails so that I can retry.
	•	Story 6.1.2 (System | High)
As the system, I want to reject files that fail antivirus or type validation.

Feature 6.2: OCR / AI Error Management
	•	Story 6.2.1 (Ops | High)
As Ops, I want low-confidence extractions flagged so that I can intervene.
	•	Story 6.2.2 (System | Medium)
As the system, I want to fall back to manual entry when extraction fails.

Feature 6.3: Audit Trail & Traceability
	•	Story 6.3.1 (Ops | High)
As Ops, I want a full audit trail of document uploads, edits, approvals, and AI actions.
	•	Story 6.3.2 (Ops | Medium)
As Ops, I want every extracted field to reference its source document.

