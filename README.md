# classkick-vuln-disclosure-2025

> Responsible disclosure record for a critical "answer interception" vulnerability in the Classkick platform.
> This repository documents discovery, timeline, and correspondence showing responsible disclosure attempts. **No exploit code or step-by-step reproduction instructions are published here.**

---

## Public report & proof files (current)

* Full report (PDF converted from original PowerPoint):
  [https://github.com/hacker123as/classkick-vuln-disclosure-2025/blob/main/I%20Cracked%20Classkick_%20My%20Story.pdf](https://github.com/hacker123as/classkick-vuln-disclosure-2025/blob/main/I%20Cracked%20Classkick_%20My%20Story.pdf)

* Classkick support reply (screenshot):
  [https://github.com/hacker123as/classkick-vuln-disclosure-2025/blob/main/classkickemail.png](https://github.com/hacker123as/classkick-vuln-disclosure-2025/blob/main/classkickemail.png)
  (Raw image: [https://raw.githubusercontent.com/hacker123as/classkick-vuln-disclosure-2025/refs/heads/main/classkickemail.png](https://raw.githubusercontent.com/hacker123as/classkick-vuln-disclosure-2025/refs/heads/main/classkickemail.png))

I will update these links/files if anything else comes out.

---

## Why this is a 0-day (and why it matters)

* **0-day definition (context):** In vulnerability terms, a “0-day” is an issue that is unknown to the vendor or has no available public fix at the time of disclosure. This issue fits the 0-day definition because it was discovered by the author, disclosed responsibly to Classkick, and—at the time of the public notes below—no public patch or mitigation has been confirmed.

* **Why this particular issue is critical:**

  * It directly exposes correct answers to clients during normal usage flows. That means the platform is effectively revealing the solution data to the same devices that students use to answer questions. This turns the platform’s normal traffic into a vector for bypassing academic integrity.
  * The exploit requires only basic browser developer tools (F12) and minimal JavaScript knowledge: no privileged access or advanced tooling required.
  * Because the vulnerability affects text-input and fill-in-the-blank question types platform-wide, the impact surface is large and affects every class, quiz, and assessment that uses those question types.
  * Detection is difficult under the current architecture because the communication looks like normal client-server traffic; server-side logs or checks may not flag it as suspicious.

* **Potential real-world harms:**

  * Widespread cheating or automated answer-filling across classes and schools.
  * Loss of trust in digital assessment platforms and possible academic consequences for students.
  * Unintended exposure of teacher-provided answers and question metadata.

---

## Summary (sanitized)

* **Vulnerability:** Answer Interception / Automatic Correct Answer Disclosure (text inputs).
* **Severity:** High to Critical.
* **Impact:** The platform sends correct answers in client-server traffic in a way that can be observed by clients, enabling automated filling of correct answers.
* **Exploitability:** Basic browser developer tools and minimal JavaScript knowledge.

> Technical exploit details and proof-of-concept code are intentionally **NOT** published here to avoid enabling abuse.

---

## What I sent to Classkick (redacted)

(Identifying fields have been redacted to protect privacy.)

> Dear Classkick Security Team,
>
> My name is [redacted]. I am a student and a cybersecurity enthusiast and researcher at Tuerss.com.
>
> I am writing to responsibly disclose a critical security vulnerability I discovered in the Classkick platform that allows students to intercept and automatically fill in correct answers without solving problems.
>
> **VULNERABILITY SUMMARY:**
> • Severity: HIGH to CRITICAL
> • Impact: Complete bypass of academic integrity for text-based questions
> • Affected: All fill-in-the-blank and text input questions platform-wide
> • Exploitability: Basic JavaScript knowledge (high school level)
>
> **TECHNICAL OVERVIEW (sanitized):**
> When students submit answers (even incorrect ones), Classkick sends the correct answers in the REQUEST PAYLOAD from the client to the server. This allows anyone with basic JavaScript knowledge to intercept these answers using browser developer tools (F12 → Console).
>
> I attached a comprehensive security report (PDF) that includes detailed discovery steps, proof-of-concept demonstrations, and recommended fixes.
>
> **CONTACT:**
> Email: [lilami@tuerss.com](mailto:lilami@tuerss.com)

---

## Timeline (select entries & dates)

* **Oct 17, 2025** — Initial responsible disclosure email sent to Classkick Security (ticket #109739), attached full report (PDF).
* **Oct 20, 2025** — Classkick Support replied: "We are not currently hiring/paying for this externally. We are aware of this and are working to improve this. We thank you for your feedback." (see `classkickemail.png`).
* **Oct 22, 2025** — Vulnerability still reproducible according to the author's tests; public notes and files uploaded to this repository for transparency.

> I will update this timeline and the repository if Classkick publishes a patch, replies with more details, or if I receive any other meaningful responses.

---

## Correspondence / attachments

Files in this repo include a `correspondence/` folder with redacted email text and screenshots. Current public files:

* `I Cracked Classkick_ My Story.pdf` (report PDF)
* `classkickemail.png` (support reply screenshot)

Example filenames to expect in `correspondence/`:

* `correspondence/2025-10-17-disclosure-email-redacted.txt`
* `correspondence/2025-10-20-classkick-reply.png`

---

## Responsible disclosure & contact

If you are a vendor, security team, or other trusted party and need the technical report, contact me at:

**[lilami@tuerss.com](mailto:lilami@tuerss.com)**

I will require a vetted contact and agreement to handle the report confidentially. I will share technical details privately with authorized parties only.

---

## Why I published this repo

* To document the responsible disclosure attempt and provide public evidence that I notified Classkick.
* To maintain a factual log of correspondence and dates.

---

## Current status

* This is a documented 0-day disclosure as of **Oct 22, 2025**. I will update this repository with new dates, responses, or patch confirmations if/when they happen.
* Public files currently hosted in this repo: the PDF report and Classkick reply screenshot (links above).

---

*If you want additional redactions, formatting changes, or a generated `SECURITY.md` with a private-reporting process, tell me and I will add them to the repo content.*
