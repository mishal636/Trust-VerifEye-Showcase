# Privacy Policy for Trust VerifEye

**Effective Date:** 25/04/2026

Thank you for choosing Trust VerifEye. This extension is independently engineered and maintained by [Mishal](https://mishal.work) ("we", "us", or "our"). We are committed to protecting your personal information and your right to privacy. This Privacy Policy explains how our Chrome Extension handles your data.

By installing and using Trust VerifEye, you agree to the practices described in this policy.

### 1. The Core Principle: 100% Local Storage
Trust VerifEye is designed with a "Privacy-First" architecture. **We do not own, rent, or operate any external servers to collect your personal data.** All data required for the extension to function is stored entirely locally on your own device within your browser's sandboxed environment.

### 2. Information We Access and How We Use It
To provide real-time phishing detection and AI analysis, our extension requires specific browser permissions. Here is exactly what we access and why:

* **Your API Key (Storage Permission):** To utilize the AI Deep Scan feature, you must provide a personal Google Gemini API key. This key is saved strictly to your browser's local storage (`chrome.storage.local`). We never transmit this key to our own servers, and we have no ability to view or access it.
* **Browsing Data (activeTab / Tabs Permission):** When you navigate to a new webpage, Trust VerifEye reads the current URL to perform security triage (checking for IP addresses, suspicious patterns, and known risks). 
* **Local Telemetry:** The extension keeps a local tally of how many sites you have scanned, blocked, or warned to generate your personal "Trust Quotient" dashboard. This history remains solely on your machine.

### 3. Third-Party Services (Google Gemini AI)
If a website is flagged as suspicious, or if you manually click the "Forced AI Deep Scan" button, the extension will send the current URL and the flagged risk factors directly to **Google's Gemini API** using your personal API Key. 
* We do not intercept or store these requests. 
* The data sent to Google is subject to Google’s own Privacy Policy and Terms of Service. Google does not use data submitted via the Gemini API to train their models.

### 4. Data Sharing and Selling
We do not collect your data, which means **we do not and cannot sell, rent, or trade your personal information or browsing history to any third parties, advertisers, or data brokers.**

### 5. Your Control Over Your Data
You have complete control over the data stored by Trust VerifEye:
* **Deleting your API Key:** You can remove your API key at any time by clicking the "Remove Key from Browser" button in the extension's Settings page.
* **Clearing Telemetry:** You can wipe all local scanning history and telemetry data simply by uninstalling the extension or clearing your Chrome browser's extension data.

### 6. Changes to This Privacy Policy
We may update this Privacy Policy from time to time to reflect changes in our practices or for operational, legal, or regulatory reasons. We will notify users of any significant changes by updating the "Effective Date" at the top of this policy.

### 7. Contact Us
If you have any questions or concerns about this Privacy Policy or our data practices, please contact the developer at: **mishalmohammed3@gmail.com**
