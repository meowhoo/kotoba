# Kotoba 隱私權政策

**最後更新日期**: 2025-11-24
**版本**: 1.0

---

## 1. 總覽

Kotoba 是一款**離線優先**的桌面小說閱讀輔助工具。我們重視您的隱私，本政策說明我們如何處理您的資料。

**核心原則**:
- ✅ 所有資料**預設儲存在您的本機電腦**
- ✅ 我們**不會收集、儲存或傳輸**您的個人資料到我們的伺服器
- ✅ 僅在您**主動使用特定功能**時，資料才會傳送給第三方服務
- ✅ 您可以**隨時停止使用**任何涉及第三方服務的功能

---

## 2. 資料收集與使用

### 2.1 我們**不會收集**的資料

Kotoba **沒有自己的伺服器**，因此我們**不會收集、儲存或分析**：
- ❌ 使用者個人身份資訊（姓名、電子郵件、電話）
- ❌ 裝置資訊或 IP 位址
- ❌ 使用行為追蹤或分析
- ❌ 您上傳的書籍內容或閱讀記錄

### 2.2 本地儲存的資料

以下資料**僅儲存在您的電腦上**，應用程式關閉後仍會保留：

| 資料類型 | 儲存位置 | 用途 |
|---------|---------|------|
| **書籍檔案** | `資料夾路徑設定/書籍資料夾/` | 儲存您匯入的書籍圖片 |
| **書籍元資料** | `meta.toml` | 書名、語言、封面等資訊 |
| **OCR 結果** | `ocr.toml` | 文字辨識結果 |
| **翻譯結果** | `translated_*.toml` | 翻譯後的文字 |
| **單字卡資料** | `vocabulary_*.toml` | 您建立的單字卡與筆記 |
| **閱讀進度** | `reading_progress.json` | 目前閱讀到第幾頁 |
| **應用程式設定** | `app-config.json` | 語言偏好、主題、資料夾路徑、API 金鑰 |

**重要提醒**:
- 您可以隨時手動刪除這些檔案
- 解除安裝應用程式**不會自動刪除**您的書籍資料

---

## 3. 第三方服務資料傳輸

當您**主動使用**以下功能時，資料會傳送給第三方服務商：

### 3.1 OCR 文字辨識（Google Cloud Vision API）

**何時傳送**:
- 您點擊「單頁 OCR」或「批次 OCR」按鈕時

**傳送的資料**:
- 📷 書籍頁面的圖片檔案（JPEG/PNG 格式）
- 🔑 您在設定中填寫的 Google Cloud API 金鑰

**第三方處理**:
- Google Cloud Vision API 會分析圖片並回傳文字
- Google 的資料使用政策：[https://cloud.google.com/terms/cloud-privacy-notice](https://cloud.google.com/terms/cloud-privacy-notice)

**如何避免**:
- 不要點擊 OCR 按鈕，則圖片不會傳送

### 3.2 AI 翻譯（LLM APIs）

**何時傳送**:
- 您點擊「翻譯當前頁」按鈕時

**傳送的資料**:
- 📝 該頁面的 OCR 文字內容（不含圖片）
- 🔑 您在設定中填寫的 API 金鑰（OpenAI/Anthropic/Google/xAI）

**第三方處理**:
- LLM 服務商會根據文字產生翻譯
- 各服務商的隱私權政策：
  - OpenAI: [https://openai.com/policies/privacy-policy](https://openai.com/policies/privacy-policy)
  - Anthropic Claude: [https://www.anthropic.com/privacy](https://www.anthropic.com/privacy)
  - Google Gemini: [https://policies.google.com/privacy](https://policies.google.com/privacy)
  - xAI Grok: [https://x.ai/legal/privacy-policy](https://x.ai/legal/privacy-policy)

**如何避免**:
- 不要點擊翻譯按鈕，則文字不會傳送

### 3.3 API 金鑰管理

**儲存方式**:
- API 金鑰以**明文形式**儲存在 `app-config.json`
- 檔案儲存在您的電腦上，僅您的作業系統使用者帳戶可以存取

**安全建議**:
- ⚠️ 請勿將 `app-config.json` 分享給他人
- ⚠️ 使用具有**最小權限**的 API 金鑰（如 Google Cloud 的「僅限 Vision API」權限）
- ⚠️ 定期在各服務商後台檢查 API 使用量

---

## 4. 資料保留與刪除

### 4.1 本地資料
- 所有資料儲存在您指定的資料夾中
- 您可以隨時手動刪除任何檔案
- 解除安裝應用程式**不會自動刪除**您的書籍資料

### 4.2 第三方服務資料
- Kotoba **無法控制**第三方服務商如何保留或刪除您的資料
- 請參考各服務商的資料保留政策
- 建議定期檢查 API 使用記錄

---

## 5. 兒童隱私

Kotoba 未設計給 13 歲以下兒童使用。我們不會故意收集兒童的個人資料。

---

## 6. 政策更新

當我們更新隱私權政策時：
- 會更新本文件的「最後更新日期」
- 在應用程式內顯示通知（如適用）
- 繼續使用應用程式即表示您同意更新後的政策

---

## 7. 您的權利

由於所有資料儲存在您的電腦上，您擁有**完全控制權**：

- ✅ **存取權**：隨時開啟檔案檢視資料
- ✅ **修改權**：手動編輯 TOML/JSON 檔案
- ✅ **刪除權**：刪除任何檔案或資料夾
- ✅ **可攜權**：複製檔案到其他裝置
- ✅ **停止使用權**：解除安裝應用程式

---

## 8. 聯絡我們

如果您對隱私權政策有任何疑問：

- 📧 電子郵件：[您的聯絡信箱]
- 🐛 問題回報：[https://github.com/[your-repo]/issues](https://github.com/[your-repo]/issues)
- 📄 專案文檔：[GitHub Repository URL]

---

## 9. 同意聲明

使用 Kotoba 即表示您已閱讀並同意本隱私權政策。

**特別提醒**:
- 您需要自行向 Google Cloud、OpenAI 等服務商註冊並取得 API 金鑰
- 使用第三方 API 時，您需遵守各服務商的使用條款
- API 使用可能產生費用，請定期檢查帳單
