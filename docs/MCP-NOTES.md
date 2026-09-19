# MCP 實作紀錄

2026-09-19 透過 Microsoft Learn 的 HTTP MCP 端點，實際呼叫 tools/list、microsoft_docs_search 與 microsoft_docs_fetch，搜尋深色模式與色彩對比。

## 官方文件重點

- 使用 prefers-color-scheme 判斷系統偏好，並保留使用者的手動選擇。
- 分別模擬 light 與 dark；不能只驗證其中一個主題。
- 以 Edge DevTools 的 Rendering 工具切換配色，以 Issues 與 Color Picker 檢查文字對比。
- 也要檢查 hover 等互動狀態。

來源：
- https://learn.microsoft.com/microsoft-edge/devtools/accessibility/test-dark-mode
- https://learn.microsoft.com/microsoft-edge/devtools/accessibility/preferred-color-scheme-simulation
- https://learn.microsoft.com/microsoft-edge/devtools/accessibility/color-picker

## 現有樣式檢視

styles.css 已使用 CSS 變數與 prefers-color-scheme；app.js 提供儲存偏好。深色主文字及次要文字分別為 #e6edf3、#8b949e，背景為 #161b22。需要特別留意綠色按鈕 hover 的白字對比，不能以深色背景本身判定全頁均合格。

## 執行方式

本次由 Codex 依教材允許的 solutions 備援路徑完成，Microsoft Learn 經 HTTP MCP 實際呼叫。GitHub 作業使用已登入 ijbhxhu 的 gh CLI。已提供 VS Code 的 Microsoft Learn 與 GitHub MCP 設定；VS Code UI 的 Running 狀態與 Copilot 對話未代稱為已驗證。
