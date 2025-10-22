# classkick-vuln-disclosure-2025

> Responsible disclosure record for a critical "answer interception" vulnerability in the Classkick platform.
> This repository documents discovery, timeline, and correspondence showing responsible disclosure attempts. **No exploit code or step-by-step reproduction instructions are published here.**

---

## 📁 Public report & proof files (current)

* **Full report (PDF):**
  [I Cracked Classkick: My Story.pdf](https://github.com/hacker123as/classkick-vuln-disclosure-2025/blob/main/I%20Cracked%20Classkick_%20My%20Story.pdf)

* **Classkick support reply (screenshot):**
  [classkickemail.png](https://github.com/hacker123as/classkick-vuln-disclosure-2025/blob/main/classkickemail.png)

**Embedded preview (screenshot)**

![Classkick support reply screenshot](https://raw.githubusercontent.com/hacker123as/classkick-vuln-disclosure-2025/refs/heads/main/classkickemail.png)

> NOTE: You can click the image above to open the original screenshot on GitHub.

**Embedded link to the PDF (preview link)**

You can preview the PDF in GitHub directly by clicking the report link above. For quick access:

[I Cracked Classkick: My Story (PDF) — open in GitHub](https://github.com/hacker123as/classkick-vuln-disclosure-2025/blob/main/I%20Cracked%20Classkick_%20My%20Story.pdf)

---

## 🔥 Why this is a 0-day (and why it matters)

**0-day explained (simple analogy):** Imagine a wall built from many bricks. Most of the time the wall stands because every brick is in place. A **0-day** is like discovering that **one brick is missing** — a single overlooked weak point that nobody noticed. If you poke or remove any other key brick, the wall can collapse. That missing brick gives someone a way to break the wall. In security terms: a 0-day is a vulnerability that **the vendor has not yet fixed** and that attackers could use immediately.

**Why this issue fits that description:**

* It was discovered by the author and responsibly disclosed to Classkick, but no public patch or mitigation had been confirmed as of the dates below — so it qualifies as a 0-day at that time. ⚠️
* The vulnerability exposes correct answers in normal client-server traffic, effectively revealing the solution to the same students using the system.
* Exploitable with only basic browser dev tools and minimal JavaScript knowledge — no advanced access needed.
* Wide impact: affects all fill-in-the-blank / text-input question types platform-wide.

**Real-world consequences:**

* Automated cheating and loss of academic integrity 📉
* Potential reputational damage to schools and to the platform 🏫
* Teacher answers and assessment integrity exposed

---

## 📝 Summary (sanitized)

* **Vulnerability:** Answer Interception / Automatic Correct Answer Disclosure (text inputs)
* **Severity:** High — Critical
* **Impact:** Correct answers are transmitted in a way that clients can observe and use
* **Exploitability:** Basic browser developer tools + simple JavaScript

> Technical exploit details and proof-of-concept code are intentionally **NOT** published here to avoid enabling abuse.

---

## ✉️ What I sent to Classkick (redacted)

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

## 📅 Timeline (select entries & dates)

* **Oct 17, 2025 — 11:26 PM CDT** — Initial responsible disclosure email sent to Classkick Security (ticket #109739), attached full report (PDF).
* **Oct 20, 2025 — 10:43 AM CDT** — Classkick Support replied: *"We are not currently hiring/paying for this externally. We are aware of this and are working to improve this. We thank you for your feedback."* (see screenshot above).
* **Oct 22, 2025** — Vulnerability still reproducible according to the author's tests; documented as a public 0-day disclosure in this repo.

> I will update this timeline and the repository if Classkick publishes a patch, replies with more details, or if I receive any other meaningful responses. 🔁

---

## 📂 Current public files in this repo

* `I Cracked Classkick_ My Story.pdf` (report PDF)
* `classkickemail.png` (support reply screenshot)

---

## 🔒 Responsible disclosure & contact

If you are a vendor, security team, or other trusted party and need the technical report, contact me at:

**[lilami@tuerss.com](mailto:lilami@tuerss.com)**

I will require a vetted contact and agreement to handle the report confidentially. I will share technical details privately with authorized parties only.

---

## ❓ Why I published this repo

* To document the responsible disclosure attempt and provide public evidence that I notified Classkick. ✅
* To maintain a factual log of correspondence and dates.

---

## 📌 Current status

* Documented as a 0-day disclosure as of **Oct 22, 2025**. I will update this repository with new dates, responses, or patch confirmations if/when they occur.
* Public files currently hosted in this repo: the PDF report and Classkick reply screenshot (links and preview above).
