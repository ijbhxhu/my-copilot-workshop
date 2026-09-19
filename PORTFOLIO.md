![工作坊完成徽章](https://img.shields.io/badge/GitHub_Copilot_實戰工作坊-已完成-1F883D?style=for-the-badge&logo=githubcopilot&logoColor=white)

# ijbhxhu 的待辦清單作品集

依 GitHub Copilot 實戰工作坊教材完成的純前端待辦清單，涵蓋 Agent 工作流程、MCP 文件查詢及 issue → PR → 合併的完整開發流程。

## 線上展示

https://ijbhxhu.github.io/my-copilot-workshop/

## 功能

- 新增、完成／取消完成、刪除待辦，忽略空白輸入。
- 全部／未完成／已完成篩選，重新整理保留偏好；無效偏好安全回退。
- 深色／淺色切換，記住手動偏好，首次載入跟隨系統。
- localStorage 保存資料，未完成計數不受篩選影響。
- 篩選隱藏項目時提供清楚提示與螢幕閱讀器狀態訊息。
- 清除已完成前需確認；沒有已完成項目時停用按鈕。
- 手機版面、鍵盤可操作、無框架與外部 CDN，可離線開啟。

## 技術

HTML、CSS 變數與原生 JavaScript。應用程式由 index.html、styles.css、app.js 組成，不使用套件或建置流程。

## 開發方式與紀錄

本次由 Codex 協助，依教材明確允許的 solutions 備援路徑建立基礎版本，再實作三個練習 issue。GitHub 操作使用 active account ijbhxhu 的 gh CLI，並未宣稱已在 VS Code 實際操作 Copilot Chat。

- Step 1：基本待辦功能。
- Step 2：多檔加入主題與篩選；刻意破壞 app.js 後 git restore，檔案 SHA-256 與破壞前相同。
- Step 3：配置 Microsoft Learn / GitHub MCP；實際呼叫 Microsoft Learn MCP 的工具探索、搜尋與擷取。見 [MCP 紀錄](docs/MCP-NOTES.md)。
- Step 4：建立 copilot-instructions.md 與 fix-issue.prompt.md，依讀 issue、分支、修正、測試、開 PR 流程完成三項工作。
- Step 5：三個 PR 合併 main、部署 GitHub Pages、完成作品集。

VS Code 的 MCP Running 顯示與 /fix-issue 選單屬 UI 操作，未在本次自動化中驗證。可在 VS Code 開啟本 repo 後使用提供的設定與提示詞。

## 修正與驗證

- [PR #5：篩選偏好](https://github.com/ijbhxhu/my-copilot-workshop/pull/5)
- [PR #6：取消勾選提示](https://github.com/ijbhxhu/my-copilot-workshop/pull/6)
- [PR #7：批次清除](https://github.com/ijbhxhu/my-copilot-workshop/pull/7)

Edge headless 實際瀏覽器驗證：新增、空白拒絕、文字安全呈現、完成／取消、刪除、重新整理保存、主題偏好、篩選持久化與無效值、狀態提示、批次確認／取消、390px 手機寬度及無 JavaScript 例外。各 PR 另附手動驗證步驟。

## 本次練習涵蓋的觀念

1. Agent 能跨檔案修改並根據執行結果修正。
2. MCP 以統一介面連接外部工具與最新文件。
3. 修改前保存 checkpoint，未提交修改可以 git restore 還原。
4. instructions 與 prompt 檔能讓工作流程版本化與重複使用。
5. 以測試、PR 與部署證據驗證成果；工作坊認證徽章仍由主辦方發放。

五題測驗答案：C、B、A、B、D。說明見 [教材解析](docs/quiz.md)。
