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
