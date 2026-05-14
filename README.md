<div align="center">

<img src="banner.svg" alt="Trust VerifEye Banner" width="100%">

<br>

[![Google Chrome](https://img.shields.io/badge/Chrome_Extension-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white)](#)
[![Gemini API](https://img.shields.io/badge/AI-Google_Gemini-8E75B2?style=for-the-badge&logo=googlebard&logoColor=white)](#)
[![Security](https://img.shields.io/badge/Security-Blue_Team-10b981?style=for-the-badge&logo=shield&logoColor=white)](#)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](#)

*Acting as a real-time Security Operations Center (SOC) inside your browser with a strict 'Bring Your Own Key' (BYOK) architecture.*

</div>

<br>

> **Trust VerifEye** is a localized, privacy-first Chrome Extension that acts as a personal Security Operations Center (SOC) analyst for everyday users. It evaluates domain integrity in real-time and leverages Large Language Models (LLMs) to detect sophisticated phishing attempts, fake stores, and structural web risks.

![Trust VerifEye Dashboard](<img width="424" height="640" alt="trustverifeye" src="https://github.com/user-attachments/assets/baf6845d-a317-420b-acee-0cadf322f5e0" />)
*View the live extension on the [Chrome Web Store]([INSERT_WEB_STORE_LINK_HERE]).*

---

## 🚀 The Architecture (How it Works)

Unlike traditional blocklists that rely on outdated databases, Trust VerifEye uses a **Two-Stage Triage Engine** to evaluate websites dynamically.

> 🧠 **Want to see under the hood?** Read the full [Architecture & Engineering Post-Mortem](ARCHITECTURE.md) for a deep dive into the triage engine, performance optimizations, and security audits.

### Phase 1: 100-Point Heuristic Triage
Before any network calls are made, the background service worker evaluates the current URL against a strict physical structural check:
- **IP Address Resolution:** Flags domains bypassing DNS mapping.
- **Top-Level Domain (TLD) Threat Intel:** Docks points for historically abused extensions (`.zip`, `.tk`, `.xyz`).
- **Shared Hosting Detection:** Identifies unverified subdomains on platforms often abused for temporary phishing (e.g., `vercel.app`, `github.io`).
- **Brand Mismatching:** Cross-references URL substrings against regional enterprise brands to catch typo-squatting.

### Phase 2: AI Waterfall Analysis
If a website scores below the safety threshold (80/100), the extension initiates a localized API call to Google's **Gemini AI**.
- **Contextual Judgment:** Acts as a SOC analyst to review flagged metadata. If the AI determines a flagged site is actually a legitimate organizational portal or safe developer tool, it triggers a **Purple 'AI Vouched' Override**.
- **Plain-English Explanations:** Explains the specific risks (or reasons for safety) to the user in actionable human language.
- **Threat Intel Export:** Generates one-click markdown reports of technical flags and AI summaries for IT ticketing.
- **Smart Caching:** Implements a caching layer (24-hour TTL) to minimize redundant API calls and optimize performance.

---

## 🛠 Tech Stack & Engineering Highlights

This project was built entirely with vanilla web technologies to maintain an ultra-lightweight footprint and zero dependencies.

- **Core:** JavaScript (ES6+), HTML5, CSS3.
- **Extension API:** Chrome Manifest V3 (Service Workers, Local Storage, Messaging API).
- **AI Integration:** Google Gemini REST API waterfall (`flash-lite-preview` → `flash` → `2.5-flash`).
- **UI/UX:** Custom Glassmorphism 2.0, dual-font typography system (Raleway/Inter), and localized state management.

---

## 🔒 Privacy & Security (Zero-Telemetry Design)

As a cybersecurity tool, user privacy is the foundational design principle. 

* **Bring Your Own Key (BYOK):** The extension operates strictly on a BYOK model, requiring the user to input their own free Gemini API key. 
* **100% Local Sandboxing:** The API key, Trusted Domain lists, and all historical telemetry (Trust Quotient, sites blocked, recent activity) are stored exclusively in `chrome.storage.local`. 
* **No Dev-Tracking:** No data, browsing history, telemetry, or analytics are *ever* transmitted to the developer or third-party servers.

---

## 📸 Interface Showcase

| 🟡 Warning State | 🔴 Critical Block | 🟣 AI Vouched (Safe) |
|:---:|:---:|:---:|
| <img width="1280" height="800" alt="warningstate" src="https://github.com/user-attachments/assets/88c88768-760e-4118-9e6e-8a39037ca7da"> | <img width="1280" height="800" alt="criticalstate" src="https://github.com/user-attachments/assets/585aab81-0460-48dd-bbb5-b15d1fe782cb"> | <img width="1280" height="800" alt="purplevouched" src="[INSERT_PURPLE_STATE_SCREENSHOT_HERE]"> |
| *Heuristic flags detected* | *Confirmed phishing trap* | *Flags detected, but AI verified safe* |

---

## 📊 SOC Analytics Dashboard

<div align="center">
   <img width="1280" height="600" alt="soc1_4_11zon" src="https://github.com/user-attachments/assets/3e9be97e-b7da-4a14-97ea-c5dddf03f3ac" alt="Telemetry Dashboard">
  <p><i>The localized telemetry engine tracking your personal "Trust Quotient" and 7-day risk history.</i></p>
</div>






---

*Note: The source code for this extension is kept private to protect the proprietary heuristic detection logic. However, the architecture, design patterns, and deployment are fully demonstrated via the live Web Store application.*
