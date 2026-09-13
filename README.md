# Circuit Fixer 電路維修員
歡迎來到由 **北科智慧家電維修社 (NTUT AIoTFixer)** 開發的互動遊戲：「**電路維修員 (Circuit Fixer)**」 專案庫！

本遊戲專案旨在透過無門檻的網頁解謎互動，讓新生快速體驗電路導通的邏輯與搶修的刺激感，在遊戲中玩家可挑戰最高分，並將成績即時同步至排行榜，進而吸引對硬體維修與 AIoT 科技有興趣的同學加入社團。

### 🚀 立即遊玩 (Play Now)
👉 [Circuit Fixer](https://aiotfixer.github.io/Circuit-Fixer/)

---
### 🌟 遊戲特色 (Feature)
  - 極速解謎：點擊方塊旋轉電線，找出正確的路徑，將左側的 110V 電源成功接通至右側隨機出現的家電。
  - 動態難度擴張：隨著過關次數增加，電路板網格會從 5x5 擴大至 7x7，最終達到 9x9 的極限挑戰。
  - 免安裝跨平台：純前端單檔 (Single-file) 開發，支援手機、平板觸控，以及電腦滑鼠點擊，開啟網頁即可遊玩。
  - 中英雙語 (i18n)：內建即時語言切換功能，友善外籍新生體驗。
  - 即時排行榜：內建 Top 100 排行榜，透過 GAS 實現跨域無伺服器 (Serverless) 的即時成績同步。

---
### 🎮 遊戲操作與規則 (How to Play)
  1. 開始搶修：點擊首頁「開始搶修」進入挑戰，起始倒數時間為 60 秒。
  2. 旋轉電線：使用滑鼠點擊（或手指觸控）畫面中央的電路方塊，每次點擊方塊會順時針旋轉 90 度。
  3. 導通電路：將左側的 110V AC 電源起點，透過旋轉方塊，一路連接到右側的「故障家電」（如：風扇、吹風機、果汁機）。
  4. 啟動家電：當完整通路形成，電流會亮起綠色光芒，家電將成功啟動並發出紙花特效！
  5. 過關獎勵：成功通電後，時間將自動延長 10 秒，並進入下一關。
  6. 結算上榜：當倒數計時歸零時遊戲結束。輸入您的學號，即可將成績上傳至排行榜。

---
### 💯 分數計算機制 (Scoring System)
  為了鼓勵玩家「既要快，又要精準」，單局得分由以下三個項目加總而成，關卡層數越高，加分倍率越大！
  - 過關基礎分：通關層數 (Level) × 100。只要過關必定獲得的底分。
  - 速度加分 (Time Bonus)：系統標準挑戰時間為 30 秒。若在 30 秒內過關，每省下 1 秒鐘，可獲得 10 × Level 的加分。
  - 步數加分 (Click Bonus)：系統會依據當下棋盤大小給予容錯步數（總格數的 3 倍）。若點擊次數低於容錯步數，每少點 1 次，可獲得 5 × Level 的加分。
  - 提示：在高難度的 7x7 或 9x9 關卡中保持極少步數與極快速度，分數將會呈現指數型爆發！

---
### 🛠️ 技術堆疊 (Tech Stack)
  - UI / Styling: Tailwind CSS (Utility-first CSS framework)
  - Icons: FontAwesome 6
  - Animation: CSS3 Keyframes, Transition, Canvas Confetti
  - Game Logic: Vanilla JavaScript (ES6), DFS Algorithm (保證路徑生成), BFS Algorithm (電流擴散判定)
  - Backend / API: Google Apps Script (GAS) + Google Sheets (作為 Serverless Database)
  - 本專案開發過程使用 Gemini 輔助協作。
