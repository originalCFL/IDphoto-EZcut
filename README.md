# 證件照排版與輸出

單一 HTML 網頁，使用瀏覽器端的 `@imgly/background-removal` 進行可選去背；使用者的照片會在其瀏覽器中處理。

## 使用與部署

1. 將本資料夾的所有檔案推送至公開 GitHub 儲存庫。
2. 在 GitHub repository 的 **Settings → Pages** 啟用 GitHub Pages，選取此資料夾所在的 branch / root。
3. 對外提供 GitHub Pages 網址與本儲存庫網址。儲存庫必須保持可公開取得，且不得移除 `LICENSE.md`、`NOTICE.md` 與此 README。

請用 HTTP(S) 網站（例如 GitHub Pages）部署，不建議直接以 `file://` 開啟；去背模型與 CDN 資源需要網路存取。

## 授權

本專案使用 `@imgly/background-removal`。該套件由 IMG.LY 以 GNU Affero General Public License v3.0（AGPL-3.0）提供。因此，本網站的完整對應原始碼以 **AGPL-3.0-or-later** 公開；使用、修改與再發布時，必須依該授權條款提供對應原始碼及保留授權、著作權與 NOTICE。

完整 AGPL-3.0 條文：[GNU AGPL v3.0](https://www.gnu.org/licenses/agpl-3.0.html)。IMG.LY 的上游套件與授權資訊：[background-removal-js](https://github.com/imgly/background-removal-js)。如需閉源、專有或不採用 AGPL 的部署，請向 IMG.LY 取得商業授權。

本 README 是部署指引，不構成法律意見。
