# 📯 臺中二中管樂社 GitHub (TCSSHWB)

歡迎來到臺中二中管樂社（TCSSH WIND BAND）的 GitHub！

---

## 🚀 核心專案 / Projects

### 📥 [線上劃位系統 (SR-System)](https://github.com/TCSSHWB/SR-System)
* **專案簡介：** 專為社團成果發表會的演出場地設計的線上劃位系統。
* **技術棧：** HTML5 / Bootstrap 5 / jQuery / Firebase (Firestore Live Sync)

---

## 👨‍💻 開發與維護指南 (學弟妹交接必看)

### 1. 倉庫與部署規範
* 本組織內的所有核心原始碼請保持在 **Private (私有)** 或由指導學長姐評估後公開。
* 網頁部署一律採用 **Cloudflare Pages**。若有修改程式碼並推（Push）至 `main` 分支，系統會自動重新部署。

### 2. 環境變數安全
* **絕對不要**將包含 Firebase 密鑰、API Key 的 `firebase-config.js` 直接推上公開倉庫。
* 請於 `firebase-config.js` 內，填入當屆社團申請的 Firebase 憑證。

### 3. Firebase 網域白名單
若未來有 **修改組織名稱** 或 **更換 Cloudflare Pages 部署網址**，請務必注意：
* **管理後臺登入：** 請至 **Firebase Console -> Authentication -> Settings** 中，將新的 `xxxx.pages.dev` 域名加入 **授權網域 (Authorized domains)**，否則後臺管理人員將**無法正常登入**。
* **資料庫安全防護：** 由於前臺劃位（Firestore）預設不限制網域，請至 Google Cloud Console 限制該 API Key 的使用權限（於 Google Cloud Console 設定網站之參照字串並限制為 `*.pages.dev`），以防止惡意人士盜用 API Key 刷取資料庫流量。
* 詳細操作步驟請參照[系統部署指南](https://hackmd.io/ENAsXUl7TjmyIgZGZID4Jw?view)。

---

## 👥 貢獻者與開拓者

感謝以下夥伴為臺中二中管樂社開發並建置此系統：

* **特別感謝：** [Eric Peng](https://github.com/alktw)、[Sam Liu](https://github.com/lzspriv)、[Una Lin](https://github.com/linzy531)

---

> 歡迎對網頁開發、資料庫有興趣的社員與幹部一起加入維護！
