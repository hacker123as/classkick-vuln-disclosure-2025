# classkick-vuln-disclosure-2025

> Responsible disclosure record for a critical "answer interception" vulnerability in the Classkick platform.  
> **This repository does not include exploit code or step-by-step technical instructions.** It documents the discovery, timeline, and correspondence showing responsible disclosure attempts.

---

## Summary (sanitized)
- **Vulnerability:** Answer Interception / Automatic Correct Answer Disclosure (text inputs).  
- **Severity:** High — impacts academic integrity.  
- **Impact:** The platform sends correct answers in client-server traffic in a way that can be observed by clients, enabling automated filling of correct answers.  
- **Exploitability:** Requires only basic browser developer tools and JavaScript knowledge (high-school level).  
- **Note:** Technical exploit details and proof-of-concept code are intentionally **NOT** published here to avoid enabling abuse.

---

## What I did
- Performed responsible disclosure directly to Classkick (security/support), provided technical report and a PowerPoint titled `I Cracked Classkick_ My Story.pptx`.  
- Offered assistance to test and verify fixes and requested acknowledgement and remediation.

---

## Timeline
- **Oct 17, 2025** — Initial responsible disclosure email sent to Classkick Security (ticket #109739), attached full report and presentation.  
- **Oct 20, 2025** — Classkick Support replied: *"We are not currently hiring/paying for this externally. We are aware of this and are working to improve this. We thank you for your feedback."* (see `correspondence/2025-10-20-classkick-reply.png`)  
- **Oct 22, 2025** — Vulnerability still reproducible (documented here as status update).

> See `timeline.md` for a more detailed timeline and file names of correspondence screenshots.

---

## Correspondence (redacted)
> Excerpts of emails and support replies are stored in `correspondence/`. Sensitive information has been redacted. Attachments and screenshots are dated and named for easy reference.

Examples:
- `correspondence/2025-10-17-disclosure-email.txt` — my disclosure email (redacted contact fields).  
- `correspondence/2025-10-20-classkick-reply.png` — support response screenshot.

---

## Proof & attachments
- I have a full technical report and a presentation: `I Cracked Classkick_ My Story.pptx`.  
- **These files are not published in this public repo.** If Classkick (or a vetted authority) requests them, I will supply them securely.

---

## Current status (as of 2025-10-22)
Vulnerability remains reproducible according to my tests. Classkick acknowledged awareness but has not provided a public fix or further details to me. See `correspondence/` for the acknowledgement screenshot.

---

## Responsible disclosure policy
If you are a vendor, security team, or other trusted party and need the technical report:
1. Contact: `lilami@tuerss.com` (as listed in my disclosure) OR open an issue in this repo titled `SECURITY: Request for full report — [Organization Name]`.  
2. I will require a clear contact and an agreement to handle the report confidentially.  
3. I prefer to share the full POC privately and coordinate disclosure after a fix.

**Public users:** do **not** request exploit details here. This repo purposefully avoids technical content that would enable cheating or exploitation.

---

## Why I published this repo
- To document my responsible disclosure attempts and provide public evidence that I attempted to notify Classkick.  
- To track the status and keep a neutral, factual log of correspondence and dates.

---

## What NOT to publish here
- Detailed proof-of-concept code or network packet captures that reveal secrets.  
- Step-by-step instructions for reproducing the exploit.  
- Full attachments that could be used maliciously without vetting.

---

## License
This repository content is licensed under **CC BY-NC-SA 4.0** (see `LICENSE`).  
If you need other licensing terms for collaboration, contact me.

---

## Contact
Author: **Amadu Stickler**  
Email: `lilami@tuerss.com`  
(Use the responsible disclosure procedure above.)

