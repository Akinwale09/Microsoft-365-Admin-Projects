#  Legal Document Repository with Version Control in Microsoft 365

This guide helps legal teams create a SharePoint-based document repository with version control and approval workflows to manage and track contract changes in Microsoft 365.

---

##  Prerequisites

- Microsoft 365 Business or Enterprise license
- SharePoint Admin or Site Owner permissions
- Power Automate permissions

---

##  Step 1: Create a SharePoint Document Library

1. Go to [SharePoint](https://portal.office.com)
2. Navigate to your legal SharePoint site or create a new one
3. Click **“+ New”** > **Document Library**
4. Name it `Legal Contracts`
5. Click **Create**

---

##  Step 2: Add Metadata Columns

1. Open the `Legal Contracts` library
2. Click **+ Add column** > Choose type:
   - **Choice** → `Contract Type` (e.g., NDA, Employment, Lease)
   - **Person** → `Owner`
   - **Date** → `Effective Date`
   - **Single line of text** → `Client Name`
   - **Choice** → `Status` (Draft, In Review, Approved, Rejected)
3. Save each column

---

##  Step 3: Enable Version History

1. Go to Library Settings:
   - Click **Settings (⚙️)** > **Library settings**
2. Under **Versioning Settings**:
   - Set **“Create a version each time you edit a file”** to **Yes**
   - Enable **“Require documents to be checked out before editing”** (optional)
3. Save changes

---

##  Step 4: Create Approval Workflow in Power Automate

1. Go to [Power Automate](https://make.powerautomate.com/)
2. Click **Create** > **Instant cloud flow**
3. Name: `Contract Approval Flow`
4. Trigger: `When a file is created or modified (properties only)`
5. Site and Library was set to SharePoint Legal Contracts

---

##  Step 5: Add Approval Actions

1. Add action: `Start and wait for an approval`
   - Approval type: **Approve/Reject - First to respond**
   - Title: `Approval Request`
   - Assigned to: Legal approver’s email
   - Details: Include contract metadata (supports Markdown):
     ```markdown
     **Client:** @{triggerOutputs()?['body/ClientName']}
     **Contract Type:** @{triggerOutputs()?['body/ContractType']}
     **Effective Date:** @{triggerOutputs()?['body/EffectiveDate']}
     **Owner:** @{triggerOutputs()?['body/Owner/Email']}
     [View Document](@{triggerOutputs()?['body/Link']})
     ```

---

##  Step 6: Add Condition Logic

1. Add a **Condition**:
   - `Outcome` is equal to `Approve`
2. **If Yes**:
   - Action: `Update file properties`
     - Set `Status` to **Approved**
3. **If No**:
   - Action: `Update file properties`
     - Set `Status` to **Rejected**

---

##  Step 7: Test the Workflow

1. Save the flow
2. Upload or modify a document in the library
3. Approver receives the request and responds
4. Check document status updates and version history

---

##  Step 8: Track Version History

1. Open any document in the library
2. Click the three dots (…) > **Version History**
3. View and restore previous versions as needed

---

