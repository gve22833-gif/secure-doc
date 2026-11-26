# Secure Digital Document Management System — Website Prototype

## Run locally
1. Extract the ZIP file.
2. Open `index.html` in Chrome, Edge, Firefox, or another modern browser.
3. Sign in using any username and password. Choose a role to preview the interface.

## Included screens
- Secure login (demo)
- Dashboard and document overview
- Smart document search (case ID, type, date, person, keyword)
- Document upload form with basic file-extension check
- Case register
- Audit trail
- Role-permission overview
- Document-level access checks: users without permission see an "Access restricted" dialog (with the reason) and can use "Get access" to request it; administrators approve or deny requests under Access Control

## Access rules in this demo
A user can view a document if they are an Administrator, uploaded it, were granted access, **or** their role is assigned to the document's case and their role's clearance covers its classification.
- Officer: CASE-0421, CASE-076 · up to Restricted
- Investigator: CASE-018, CASE-076 · up to Confidential
- Legal Team: CASE-0421 · up to Confidential
- Administrator: all cases

Try it: sign in as Officer → click "Get access" on a locked document → log out → sign in as Administrator → Access Control → Approve → sign in as Officer again with the same username.

## Important prototype limitation
This is a front-end demonstration. It stores sample data only in JavaScript memory for the current page session. It does not implement real user authentication, server-side authorization, encryption, persistent document storage, backups, or secure audit logging. Those require a backend, database, secure file storage, and server-side security controls before real sensitive/legal documents are used.

## Suggested next step
Connect the interface to a backend API and database; enforce role and case permissions on every server request; verify file content and metadata; encrypt files at rest and in transit; and persist audit events in tamper-resistant storage.
