V4.1: Publish complete firestore-rules-merge.txt before deploying. Existing single groups remain supported.
TWA e-KPI V2.9.1 — Firebase Cloud Edition
1. Firebase Console project ecrew-absensi-183ac: enable Authentication Email/Password and Cloud Firestore. Add hosting domain to Authentication authorized domains.
2. Merge firestore-rules-merge.txt into existing rules, do not replace other apps rules. Review overlapping wildcard allows; test in emulator before production.
3. Register admin via app (Pending). In Firebase Console Firestore ekpi_users/{UID}, set admin=true and status=Approved manually for trusted administrator. Login to initialize weights. No public admin bootstrap.
4. Deploy index.html, sw.js, manifests and icons via HTTPS. Do not publish private backup JSON. Restore old backup via Admin Backup menu; existing local accounts must register again.
5. All business data read from Firestore server; no local database. Signatures stored as compressed image data in Firestore (not Storage). Authentication session in memory. Dashboard refreshes every 30 seconds; other pages use loaded snapshot, logout/login to refresh. Internet required. Batch limit 500. Concurrent edits to same record can overwrite; review before production. No live Firebase or rules emulator test performed. User evaluation scores are client calculated; server-side score validation recommended before production.

Login password visibility toggle added.

V2.9.5: Admin may migrate legacy groups from Employee Register; existing reviews are unchanged. Assign new groups and user scopes manually. One KPI group per employee.

V2.9.5: Added Staff KPI group separately from Supporting Staff; existing records unchanged.

V3.1: Configure Job Description Management before evaluating. Templates stored in ekpi_settings/jobDescriptions. Historical snapshots preserved. Templates not included in existing JSON backup.

V3.3: automatic equal job description weight distribution on add/delete; exact cent-percent totals.

Reviewer Register requires additional admin-only Firestore rule in reviewer-rules.txt. Reviewer records are not included in legacy JSON backup.

V3.9: Admin-only individual evaluation deletion with confirmation. Existing Firestore rules unchanged.

V3.9: Click any employee row to open the existing employee detail/edit form.

V5.6: Editable job description weights, proportional redistribution with exact hundredth-percent totals.

V5.6: Employee details popup; Copy copies profile text to clipboard.

Profile photos: compressed JPEG stored in employee document.

V5.6: Purchasing job title and default Logistics / Purchasing mapping.

Department retains legacy division database key; new Division uses operationalDivision. Existing records remain unassigned until edited.

V5.6: Admin must review legacy Pilot employee mappings and user scopes. Existing history is unchanged. Legacy Pilot JD templates are fallback only until a new group template is saved.

V5.6: Separate job description, KPI target and measurement in evaluation breakdown.

V5.6: Review/approval authorized accounts can view all evaluation history.

V5.6: A4 portrait evaluation print preview for authorized users.

V5.7: Publish updated firestore-rules-merge.txt before use. Each evaluator and President Director uploads their own signature once; saved privately by UID. Existing evaluations are not retroactively signed.

V5.9: Duplicate editable draft and admin-only delete in evaluation details. Existing V5.7 rules unchanged.

V5.9: Publish rules, then Admin > Evaluator Register > Publish Registration Name List. Verify identity before approval. Republish after changes. Names and job titles are public; signatures are private.

V6.0: Publish updated rules. Admin can delete non-admin e-KPI profiles and personal signatures. Firebase Authentication accounts and historical evaluations remain.

V6.1: Returned evaluations can be revised and resubmitted by their original evaluator. Publish updated rules.

V6.2: Remove signature image borders in previews and reports. No rules changes.

V6.3: automatic signature only; horizontal clickable evaluation history. Rules unchanged.

V6.8: Justified PDF report paragraphs.

V6.8: Evaluation Details opens the native print dialog automatically after report images load. Manual print remains available.

V6.8: Employee photo in evaluation details; new reviews store photo snapshot.

V6.8: Shared admin/evaluator report layout and employee photo in print.

V6.8: live Employee Register search.
