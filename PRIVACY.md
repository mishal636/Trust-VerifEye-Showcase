# Privacy Policy for Trust VerifEye

**Effective Date:** 19/05/2026

Thank you for choosing Trust VerifEye. This extension is independently engineered and maintained. We are committed to protecting your personal information and your right to privacy through a strict "Bring Your Own Key" (BYOK) architecture. 

This Privacy Policy comprehensively discloses how our Chrome Extension collects, uses, stores, and shares your data.

## 1. Data Collection: What Information We Collect
To provide real-time phishing detection and AI analysis, Trust VerifEye collects the following information locally on your device:
* **Browsing Data (URLs):** We collect the Uniform Resource Locator (URL) of your active tab via the `activeTab` and `tabs` permissions.
* **API Key:** We collect the Google Gemini API key you manually provide in the extension settings.
* **Local Telemetry:** We collect basic usage metrics (number of sites scanned, blocked, or warned) to generate your personal "Trust Quotient" dashboard. 

## 2. Data Use: How We Handle Your Information
The data collected is used strictly for the functionality of the extension:
* **Security Triage:** The collected URL is analyzed locally to check for IP addresses, suspicious patterns, and known risks.
* **UI Injection:** Using the `<all_urls>` permission, if a high-risk domain is detected, we use the URL context to inject our visual warning banner or block-page interstitial into the page.
* **AI Deep Scan:** The URL and flagged risk factors are utilized to prompt the AI for a deep threat analysis.

## 3. Data Storage: Where Your Information Lives
Trust VerifEye operates on a 100% local storage model. We do not own, rent, or operate any external databases.
* **Local Sandboxing:** Your Gemini API key, AI verdicts, and telemetry data are stored entirely locally on your own device within your browser's sandboxed environment (`chrome.storage.local`).
* **No Developer Access:** The developer has absolutely zero visibility into your browsing habits, history, or API key.

## 4. Data Sharing: Who We Share Your Information With
We do not sell, rent, or trade your personal information or browsing history to any advertisers or data brokers. Data is only shared with the following essential third party to provide core functionality:
* **Google Gemini API:** When a deep scan is triggered (automatically or manually), or when fetching trusted regional domains, the current URL and threat indicators are transmitted directly to Google's official Gemini API endpoints using your personal API key. 
* This data is subject to Google’s own Privacy Policy and Terms of Service (Google does not use data submitted via the Gemini API to train their models). We do not intercept or proxy these requests.

## 5. User Rights and Control
You have complete control over your data:
* **Deleting Data:** You can remove your API key at any time by clicking "Remove Key from Browser" in the Settings page. You can wipe all local scanning history, caches, and telemetry data by uninstalling the extension or clearing your Chrome browser's extension data.

## 6. Contact Us
If you have any questions or concerns about this Privacy Policy or our data practices, please contact the developer at: mishalmohammed3@gmail.com
