CADET ATTENDANCE ID WEB APP - VERSION 2.3.3-ID

PURPOSE
This is the ID-based Attendance Register. QR codes must contain only a numeric cadet ID, for example: 123456. If a cadet arrives without a QR code and does not know their ID, staff may type the cadet name manually.

FEATURES
- Rear-camera QR scanning on iPhone, iPad and compatible Android devices
- QR contents expected as digits only
- Manual entry accepts either a numeric cadet ID or a cadet name
- Manually entered names are clearly marked in the on-screen attendance list
- Duplicate ID detection and duplicate manual-name detection
- Chronological or ID/name sorting
- Present count
- Home Training Parade and Other Activity types
- PCF checkbox for Other Activity records, including manual-name records
- Activity resume logic for sessions reopened within two hours
- Activity Closed mode
- Past activity viewing
- Delete one completed activity or delete all completed activities
- CSV export
- Offline app shell after the first successful online load

CSV FORMAT (SCANNER IMPORT A:E)
All CSV files contain:
ID,Manual Name,Arrival Date,Arrival Time,Entry Method

All activities export exactly the same five columns. PCF is an on-screen checklist for Other Activities only and is never exported.

ID records are exported first in arrival order. Any manually entered names are deliberately moved to the END of the CSV in their own arrival order, with the ID field blank and Entry Method set to Manual Name. This allows staff to identify and resolve them manually.

Example:
ID,Manual Name,Arrival Date,Arrival Time,Entry Method
123456,,2026-08-13,18:42:15,QR
123789,,2026-08-13,18:43:02,Manual
,Smith John,2026-08-13,18:45:11,Manual Name

DEPLOYMENT
Upload all files in this folder directly to the root of the GitHub repository:
Attendance-Register-ID

Enable GitHub Pages from the main branch and /(root).
The expected web app URL is:
https://mrqueeg.github.io/Attendance-Register-ID/

IMPORTANT
This ID version uses its own localStorage key and does not read or alter the name-based app's attendance records.
Attendance data is stored locally in the browser on each device. Export required CSV files before deleting activities or clearing website data.

VERSION 2.3.3 FIXES
- CSV exports exactly five columns for both activity types.
- PCF remains available on screen for Other Activities but is excluded from CSV.
- Exactly one newline separates CSV records; no empty spacer rows.
- Service worker cache and app version updated to load new code.
