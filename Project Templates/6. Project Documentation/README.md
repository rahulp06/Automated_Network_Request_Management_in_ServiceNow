# Automated Network Request Management

**SkillWallet ID:** SWUID2026232277  
**Project owner / demonstrator:** PILLEM RAHUL  
**GitHub repository:** https://github.com/rahulp06/Automated_Network_Request_Management_in_ServiceNow  
**Environment:** dev446474.service-now.com (ServiceNow Personal Developer Instance)

## Purpose
A ServiceNow Service Catalog workflow for network-service request intake, mandatory-variable validation, REQ/RITM traceability, approval/rejection, lifecycle notifications, and state tracking.

## Folder structure
This package mirrors the seven phases from the supplied template archive:
1. Ideation Phase
2. Requirement Analysis
3. Project Design Phase
4. Project Planning Phase
5. Project Development Phase
6. Project Documentation
7. Project Demonstration

## Ideation diagrams
- Empathy map visual and customer journey map are included in Phase 1. They are explicitly labelled as working hypotheses, not results of completed interviews or a customer survey.
- The ideation mind map shows selected capabilities and future-scope ideas.

## Verified evidence
- Catalog form blocked submission when mandatory values were absent.
- Request `REQ0010004` links to Requested Item `RITM0010005`.
- Parent Request approval and request state were both Approved.
- `RITM0010005` shows item Network Request, quantity 1, stage Request Approved, and state Open.
- Approval and rejection outcomes were tester-confirmed; the rejection test record ID was not captured.
- SMTP connection succeeded after the App Password was re-entered without spaces.
- Network Request notifications appeared in the test inbox.

## Demonstration status
- The final narrated MP4 is included under `7. Project Demonstration/` in this package.
- The repository contains the target project URL above, but the actual MP4 and documentation upload must still be completed by the project owner; add the direct MP4 URL once available.

## Known limitations / follow-ups
- Five outbound messages remained queued at the last diagnostic check; their individual states/reasons were not inspected.
- Email receiving was non-operational in diagnostics and is not needed for the verified outbound path.
- Approval and Group approvals related lists were empty on the inspected parent request; trace direct approval-record location if required for audit.
- `TASK0020173` is an unintended generic task record with blank Short description; review under cleanup policy before deleting.
- Formal performance/load testing and production mail/security review were not performed.
- Narrated screen demo has been recorded (97.97 seconds) and is included in Phase 7 as `Automated_Network_Request_Management_Demo_With_User_Voice.mp4`. The public GitHub file URL remains pending until the repository upload is completed.

## Security
No SMTP/App Password is included. Keep secrets, the full temporary inbox address, credentials, and unredacted screenshots out of GitHub and public links. Test routing is instance-wide; inspect queued mail before removing it.
