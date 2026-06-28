# 📯 臺中二中管樂社 GitHub (TCSSHWB)

歡迎來到臺中二中管樂社（TCSSH WIND BAND）的 GitHub！

> **📢 本 GitHub 組織及旗下所有專案，皆由「臺中二中管樂社之學生社員」自主建立、開發與維護，並非臺中二中學校官方（校方行政單位）之正式官方專案。**

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
* **絕對不要**將包含 Firebase 金鑰、API Key 的 `firebase-config.js` 直接推上公開倉庫。
* 請於 `firebase-config.js` 內，填入當屆社團申請的 Firebase 憑證。

### 3. Firebase 網域白名單
若未來有 **修改組織名稱** 或 **更換 Cloudflare Pages 部署網址**，請務必注意：
* **管理後臺登入：** 請至 **Firebase Console -> Authentication -> Settings** 中，將新的 `xxxx.pages.dev` 域名加入 **授權網域 (Authorized domains)**，否則後臺管理人員將**無法正常登入**。
* **資料庫安全防護：** 由於前臺劃位（Firestore）預設不限制網域，請至 Google Cloud Console 限制該 API Key 的使用權限（於 Google Cloud Console 設定網站之參照字串並限制為 `*.pages.dev`），以防止惡意人士盜用 API Key 刷取資料庫流量。
* 詳細操作步驟請參照[系統維護與部署指南](https://hackmd.io/@lzspriv/tcsshwb-sr-system-guide)。

---

## 🛑 組織專案與技術免責聲明

1. **技術局限與現況授權（AS-IS）**：本組織內之專案（如 SR-System）皆為學生社員自學之階段性基礎開發成果，採用輕量化架構開發。原創團隊已盡可能提高系統安全性，但所有專案皆依據 MIT 許可證**以現況（AS-IS）提供原始碼與授權，不保證程式碼完全無誤、亦不承擔任何後續無償維護、Bug 修正或永久營運之義務。**
2. **營運責任切割與法律免責**：原創開發團隊僅負責「基礎系統建置與初期技術交接」。後續各屆專案之正式部署、正式發表會線上劃位營運、資料庫管理、觀眾個人資料維護（包含個資法規範之落實與按時銷毀）等實際營運行為，**其所衍生之所有資安漏洞、個資外洩風險及相關法律責任，一律由「當屆社團營運幹部與該屆網頁實際負責人」自行承擔，與原創開發者完全無關。**

---

## 👥 貢獻者與開拓者

感謝以下夥伴為臺中二中管樂社開發並建置此系統：

* **特別感謝：** [Eric Peng](https://github.com/alktw)、[Sam Liu](https://github.com/lzspriv)、[Una Lin](https://github.com/linzy531)

---

> 歡迎對網頁開發、資料庫有興趣的社員與幹部一起加入維護！
