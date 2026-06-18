# Project 3: Phishing Awareness Analysis

**DecodeLabs Industrial Training | Cyber Security | Batch 2026**  
**Author:** Devki Prajapati

---

## Overview

This project involved analyzing sample emails to identify phishing attempts using a **self-built Phishing Email Analyzer** web application. The tool automatically detects red flags in any email and returns a color-coded verdict — helping users recognize and avoid phishing attacks.

---

## Objective

Analyze sample emails to identify phishing attempts using a self-built detection tool.

---

## The Tool I Built

A fully working **Phishing Email Analyzer** web application built from scratch using **HTML and JavaScript**.

### Features:
- Runs completely **offline** in any browser — no internet required
- **6 preloaded sample emails** — 4 phishing and 2 safe
- User can paste any real or sample email and click **Check Email**
- Automatically scans for **6 types of red flags**
- Returns a **color-coded verdict**: `SAFE`, `SUSPICIOUS`, or `PHISHING`
- Displays every red flag found with a clear explanation
- Provides a **recommended action** for the user to follow

---

## Types of Phishing Attacks

Phishing attacks are categorized into three levels based on how targeted they are:

| Type | Description |
|---|---|
| **Mass Phishing** | Generic fake emails sent to millions of people, mimicking popular brands like Amazon or PayPal. High volume but low personalization. |
| **Spear Phishing** | Highly targeted attack using personal details gathered from LinkedIn or company websites to appear legitimate and trustworthy. |
| **Whaling** | Attacks aimed directly at CEOs and senior executives to authorize large wire transfers or leak confidential business documents. |

**Additional channels:** SMS attacks (Smishing), Voice call attacks (Vishing), QR code attacks (Quishing), and fake search results (Search Engine Phishing).

---

## Test Results

### TEST 1 — PayPal Phishing Email
- **Subject:** URGENT: Your account has been suspended!
- **Sender:** security@secure-paypa1.com
- **Result:** 🔴 PHISHING — 5 red flags detected

| Red Flag | Detail |
|---|---|
| Fake Domain | `paypa1.com` instead of `paypal.com` |
| Urgency Language | "within 24 hours", "immediately" |
| Sensitive Action Requested | Asked to verify personal details |
| Suspicious URL | `paypal-secure-login.xyz` is not a real PayPal domain |
| Generic Greeting | "Dear Customer" instead of the user's real name |

**Action:** Block sender. Report to security team. Do not click, reply, or open any attachments.

---

### TEST 2 — CEO Wire Transfer Email (BEC Attack)
- **Subject:** IMMEDIATE ACTION REQUIRED: Transfer Authorization
- **Sender:** ceo.urgent@executive-update.com
- **Result:** 🔴 PHISHING — 4 red flags detected

| Red Flag | Detail |
|---|---|
| Fake Sender Domain | `executive-update.com` is not a company domain |
| Urgency Language | "immediately", "time sensitive" |
| Secrecy Demand | "do not discuss with anyone" |
| Bypass Demand | "bypass standard procedure" |

> This is called a **Business Email Compromise (BEC) attack** — one of the most financially damaging types of phishing.

**Action:** Block sender. Escalate to security team immediately. Verify with CEO through a separate channel.

---

### TEST 3 — Microsoft Password Expiry Email
- **Subject:** Mandatory: Password expires in 24 hrs
- **Sender:** it-support@microsofft-helpdesk.com
- **Result:** 🔴 PHISHING — 4 red flags detected

| Red Flag | Detail |
|---|---|
| Fake Domain | `microsofft` is misspelled — not the real Microsoft domain |
| Urgency Language | "expires in 1 hour", "act now or account will be locked" |
| Suspicious URL | `microsoft.login-update.net` is not a real Microsoft link |
| Sensitive Action | Asked to reset password through an unverified external link |

> This is called a **Credential Harvesting attack** — designed to steal your login details.

**Action:** Do not click the link. Go directly to microsoft.com to check your account.

---

### TEST 4 — Team Project Update (Safe Email)
- **Sender:** sarah.lee@company.com
- **Subject:** Q3 Project Status Update - Non-Urgent
- **Expected:** Safe → **Result:** 🟡 SUSPICIOUS — 1 flag triggered

**Observation:** The tool flagged this as suspicious due to a minor keyword match. This shows that **no automated tool is perfect** — human judgment is always the final layer of defense. A real analyst would review this and mark it safe.

---

### TEST 5 — Google Security Notice (Safe Email)
- **Sender:** no-reply@accounts.google.com
- **Subject:** Your Google Account password was changed
- **Expected:** Safe → **Result:** 🟢 SAFE — 0 red flags found ✅

The tool correctly identified this as a legitimate email: domain matched, no urgency, no suspicious links, no sensitive requests.

---

##  The 6 Red Flags Checklist

Every email should be checked against these 6 red flags before taking any action:

| # | Red Flag | What to Look For |
|---|---|---|
| 1 | **Suspicious or Fake Domain** | Brand name is misspelled or domain does not match the real company |
| 2 | **Urgency or Pressure Language** | Phrases like "act now", "within 24 hours", "account will be suspended" |
| 3 | **Sensitive Action Requested** | Asking for password, payment details, or personal information via email |
| 4 | **Secrecy or Bypass Demand** | Instructing you to keep it confidential or skip normal procedures |
| 5 | **Suspicious Link or URL** | Link does not match the official brand domain when read from right to left |
| 6 | **Generic Greeting** | Says "Dear Customer" or "Dear User" instead of addressing you by name |

> **If even one of these is found — pause, verify through a separate channel, and report.**

---

## Key Takeaways

- Automated tools are a strong **first layer** of defense, but human judgment remains essential
- The most dangerous phishing emails combine **urgency + secrecy + fake domain** together
- BEC (Business Email Compromise) attacks are financially the most damaging type
- Always verify sensitive requests (wire transfers, password resets) through a **separate, trusted channel**

---

## Conclusion

**Project 3 Successfully Completed!**

This project demonstrated how real-world phishing attacks work, how to build an automated detection tool, and why a combination of both technology and human awareness is needed for effective cybersecurity defense.

---

*Devki Prajapati | DecodeLabs Industrial Training | Cyber Security | Batch 2026*
