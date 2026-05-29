Arshana Shyamkishore & Associates
Official Website & Secure Client Portal
> *Defenders of Rights · Legal Architects · Guardians of Justice*
---
Overview
This repository contains the complete official website for Arshana Shyamkishore & Associates, a professional law firm based in KwaZulu-Natal, South Africa. The site includes a full public-facing practice website, a secure client document portal, and a private administration panel — all hosted on GitHub Pages at zero cost.
Built with precision, care, and a commitment to excellence by KTech ICT.
---
Pages
File	Description
`index.html`	Main public website — services, team, CEO profile, contact
`login.html`	Secure client login portal
`portal.html`	Client document dashboard — access Google Drive folders
`admin.html`	Private administration panel — manage clients and Drive links
---
Features
Public Website
Full practice profile with services, team bios and CEO biography
Animated service carousel with 8 practice areas including Taxation & Bills
Responsive layout built on the Nicepage framework
Direct contact section with prominent phone and email
Client Portal
Email and password authentication managed by the office
Four dedicated document folder categories linked to Google Drive:
📁 Recordings & Telecon Slips
📁 Consultation Notes
📁 Perused Documents
📁 Accounts
Client-specific folder overrides for dedicated sub-folders
Show / hide password toggle
Forgot password flow directing clients to the office
No file size limits — powered by Google Drive storage
Admin Panel
SHA-256 hashed admin password — real password never stored in source code
Add, edit and remove client accounts
Assign individual Google Drive folder links per client
Client-specific folder override system
Show / hide password toggles on all credential fields
Full client overview dashboard with document counts
View Website shortcut from within the panel
---
Security
This project was built with a layered security approach appropriate for a professional legal practice hosted on a static platform.
🔒 SHA-256 Password Hashing
The admin panel password is never stored in plain text anywhere in the codebase. It is stored exclusively as a SHA-256 cryptographic hash. Even with full access to the source code, the hash cannot be reversed to reveal the original password.
🔒 Session-Based Client Authentication
Client sessions are managed using `sessionStorage` which is automatically cleared when the browser tab is closed. Clients cannot remain permanently logged in across sessions.
🔒 localStorage Client Database
Client credentials and portal configuration are stored in the browser's `localStorage` on the administrator's office device only. This data is never transmitted to any server, never committed to this repository, and never visible in the source code.
🔒 Google Drive Secure Storage
All legal documents are stored in Google Drive under the firm's Google One account. Documents are shared at the folder level using Google's "Anyone with the link" permission model — the same enterprise-grade access control used by legal and financial institutions globally. No documents are stored in this repository.
🔒 No Backend Exposure
Because this is a fully static site with no server, database, or API, there is no backend attack surface. There are no SQL injection vectors, no server-side vulnerabilities, and no credentials transmitted over a network.
🔒 HTTPS Enforced
GitHub Pages enforces HTTPS on all traffic by default, ensuring all communication between the client browser and the site is encrypted in transit.
---
Deployment
This site is deployed via GitHub Pages from the `main` branch. Changes pushed to `main` are automatically reflected on the live site within approximately 60 seconds.
Recommended Workflow
Use GitHub Desktop (`desktop.github.com`) for all updates:
Make changes to your local cloned folder
Open GitHub Desktop — changed files are listed automatically
Write a brief commit message
Click Commit to main then Push origin
No manual file management required.
---
Changing the Admin Password
To update the admin password at any time:
Open your browser console on any webpage (`F12` → Console)
Run the following, replacing `YourNewPassword` with your chosen password:
```javascript
crypto.subtle.digest('SHA-256', new TextEncoder().encode('YourNewPassword'))
  .then(b => console.log([...new Uint8Array(b)].map(x => x.toString(16).padStart(2,'0')).join('')))
```
Copy the output hash
Open `admin.html` and find the line:
```javascript
const ADMIN_HASH = '...';
```
Replace the hash string with your new one
Save and push to GitHub
---
File Structure
```
/
├── index.html                              # Main website
├── login.html                              # Client login
├── portal.html                             # Client document portal
├── admin.html                              # Admin panel
├── nicepage.css                            # Nicepage framework styles
├── index.css                               # Homepage styles
├── nicepage.js                             # Nicepage framework scripts
├── jquery.js                               # jQuery
├── ktech-logo.jpeg                         # KTech ICT logo
├── Designer__3_.png                        # KT Tech ICT badge
├── Untitled_video_-_Made_with_Clipchamp.gif # HTML King Protect animation
├── images/
│   ├── 1663533747_151635_fs-removebg-preview.png  # Firm logo
│   ├── 2021-06-17.webp                            # CEO portrait
│   ├── pexels-*.jpg / photo-*.jpeg                # Background images
│   └── *.png                                      # Service icons
└── README.md                               # This file
```
---
Important Notes
Client data is browser-local. If you clear your browser storage or switch computers, client accounts will need to be re-entered in the admin panel. Keep a private offline backup of your client list.
Drive folder links are "anyone with the link" — treat them as you would any confidential document link and do not share them outside the portal.
This repository should remain public for GitHub Pages free hosting. The security model is designed with this in mind — no sensitive data is ever committed to the repo.
---
Contact
Arshana Shyamkishore & Associates
📞 031 464 4940
📧 arshanasnlaw@gmail.com
---
<br>
---
```
╔══════════════════════════════════════════════════════════════╗
║                                                              ║
║          Designed, Engineered & Secured with Excellence      ║
║                                                              ║
║                     K T E C H   I C T                        ║
║                   Web Design & Development                   ║
║                                                              ║
║              HTML King Protect  ·  Ver 10.9                  ║
║                                                              ║
║   Enterprise-grade web solutions for legal professionals.    ║
║   Built with precision. Secured with integrity.              ║
║   Delivered with excellence.                                 ║
║                                                              ║
╚══════════════════════════════════════════════════════════════╝
```
© 2026–2027 KTech ICT · All rights reserved
Built for Arshana Shyamkishore & Associates · KwaZulu-Natal, South Africa
