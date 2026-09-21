# VOG-Business-Registry

## Build Plan: Survey123 + SharePoint + Power Automate

1. **Define data model**
   - List required fields (business name, registration ID, owner, status, dates, attachments).
   - Map each field to both Survey123 question types and SharePoint column types.

2. **Set up SharePoint list**
   - Create a list for business registry records.
   - Add columns matching the agreed data model.
   - Configure permissions for submitters, reviewers, and admins.

3. **Build Survey123 form**
   - Create form with required validation, dropdowns, and attachment support.
   - Add hidden/system fields (submission timestamp, submitter email, unique record key).
   - Publish and test on web and mobile.

4. **Integrate Survey123 to SharePoint**
   - Use Power Automate trigger for new Survey123 responses.
   - Create/update SharePoint list items from Survey123 payload.
   - Handle file attachments and value transformations (dates, choice values, IDs).

5. **Implement workflow automation**
   - Build Power Automate approval flow (new submission → review → approve/reject).
   - Update SharePoint status fields and audit trail at each stage.
   - Send notifications to submitter and reviewers.

6. **Add exception handling and logging**
   - Create failure branch in flows with error details.
   - Log failed transactions in a SharePoint log list or Teams channel.
   - Add retry policy for transient connector failures.

7. **Security and governance**
   - Use least-privilege service/account connections.
   - Apply data retention, sensitivity labeling, and access controls.
   - Document ownership, support contacts, and change management process.

8. **Testing and release**
   - Run end-to-end test cases (valid, invalid, duplicate, and attachment-heavy submissions).
   - Validate approval outcomes and notification content.
   - Promote to production with rollback steps and post-release monitoring.