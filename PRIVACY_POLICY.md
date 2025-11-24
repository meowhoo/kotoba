# Kotoba Privacy Policy

**Last Updated**: November 24, 2025
**Version**: 1.0

---

## 1. Overview

Kotoba is an **offline-first** desktop reading assistant for novels. We respect your privacy and this policy explains how we handle your data.

**Core Principles**:
- ✅ All data is **stored locally on your computer by default**
- ✅ We **do not collect, store, or transmit** your personal data to our servers
- ✅ Data is only sent to third-party services when you **actively use specific features**
- ✅ You can **stop using** any features involving third-party services at any time

---

## 2. Data Collection and Use

### 2.1 Data We **Do Not Collect**

Kotoba **has no backend servers**, so we **do not collect, store, or analyze**:
- ❌ Personal identification information (name, email, phone)
- ❌ Device information or IP addresses
- ❌ Usage behavior tracking or analytics
- ❌ Your uploaded book content or reading history

### 2.2 Locally Stored Data

The following data is **stored only on your computer** and persists after closing the application:

| Data Type | Storage Location | Purpose |
|-----------|------------------|---------|
| **Book Files** | `Data Folder/Books/` | Store imported book images |
| **Book Metadata** | `meta.toml` | Book title, language, cover info |
| **OCR Results** | `ocr.toml` | Text recognition results |
| **Translation Results** | `translated_*.toml` | Translated text |
| **Vocabulary Cards** | `vocabulary_*.toml` | Your created flashcards and notes |
| **Reading Progress** | `reading_progress.json` | Current reading page |
| **App Settings** | `app-config.json` | Language preference, theme, folder paths, API keys |

**Important Notes**:
- You can manually delete these files at any time
- Uninstalling the app **will not automatically delete** your book data

---

## 3. Third-Party Service Data Transmission

Data is sent to third-party services only when you **actively use** the following features:

### 3.1 OCR Text Recognition (Google Cloud Vision API)

**When Data is Sent**:
- When you click "Single Page OCR" or "Batch OCR" buttons

**Data Sent**:
- 📷 Book page image files (JPEG/PNG format)
- 🔑 Your Google Cloud API key configured in settings

**Third-Party Processing**:
- Google Cloud Vision API analyzes images and returns text
- Google's data usage policy: [https://cloud.google.com/terms/cloud-privacy-notice](https://cloud.google.com/terms/cloud-privacy-notice)

**How to Avoid**:
- Do not click OCR buttons, and images will not be sent

### 3.2 AI Translation (LLM APIs)

**When Data is Sent**:
- When you click the "Translate Current Page" button

**Data Sent**:
- 📝 OCR text content of that page (no images)
- 🔑 Your API key configured in settings (OpenAI/Anthropic/Google/xAI)

**Third-Party Processing**:
- LLM service providers generate translations based on text
- Privacy policies of each provider:
  - OpenAI: [https://openai.com/policies/privacy-policy](https://openai.com/policies/privacy-policy)
  - Anthropic Claude: [https://www.anthropic.com/privacy](https://www.anthropic.com/privacy)
  - Google Gemini: [https://policies.google.com/privacy](https://policies.google.com/privacy)
  - xAI Grok: [https://x.ai/legal/privacy-policy](https://x.ai/legal/privacy-policy)

**How to Avoid**:
- Do not click translate buttons, and text will not be sent

### 3.3 API Key Management

**Storage Method**:
- API keys are stored **in plain text** in `app-config.json`
- The file is stored on your computer, accessible only to your OS user account

**Security Recommendations**:
- ⚠️ Do not share `app-config.json` with others
- ⚠️ Use API keys with **minimal permissions** (e.g., Google Cloud "Vision API only")
- ⚠️ Regularly check API usage in each provider's dashboard

---

## 4. Data Retention and Deletion

### 4.1 Local Data
- All data is stored in folders you specify
- You can manually delete any files at any time
- Uninstalling the app **will not automatically delete** your book data

### 4.2 Third-Party Service Data
- Kotoba **cannot control** how third-party providers retain or delete your data
- Please refer to each provider's data retention policy
- We recommend regularly checking API usage logs

---

## 5. Children's Privacy

Kotoba is not designed for children under 13 years old. We do not knowingly collect personal data from children.

---

## 6. Policy Updates

When we update this privacy policy:
- We will update the "Last Updated" date in this document
- Display notifications in the app (if applicable)
- Continued use of the app indicates your acceptance of the updated policy

---

## 7. Your Rights

Since all data is stored on your computer, you have **full control**:

- ✅ **Access Right**: Open files to view data at any time
- ✅ **Modification Right**: Manually edit TOML/JSON files
- ✅ **Deletion Right**: Delete any files or folders
- ✅ **Portability Right**: Copy files to other devices
- ✅ **Right to Stop Using**: Uninstall the application

---

## 8. Contact Us

If you have any questions about this privacy policy:

- 📧 Email: [Your Contact Email]
- 🐛 Issue Reports: [https://github.com/[your-repo]/issues](https://github.com/[your-repo]/issues)
- 📄 Project Documentation: [GitHub Repository URL]

---

## 9. Consent Statement

By using Kotoba, you acknowledge that you have read and agreed to this Privacy Policy.

**Special Reminders**:
- You need to register with Google Cloud, OpenAI, etc., and obtain API keys yourself
- When using third-party APIs, you must comply with each provider's terms of service
- API usage may incur charges; please check your bills regularly
