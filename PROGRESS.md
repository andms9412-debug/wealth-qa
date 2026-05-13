# wealth-qa 進度紀錄（SSOT）

> 依 CLAUDE.md「計畫進度紀錄協議」：本檔 = 此專案進度的單一事實來源。
> Fresh session 進入專案必讀此檔。Milestone 完成立即 append 到 Timeline + 同步 update Plan Status 段。

---

## 專案定位

**核心交付物**：理專月會 10 題救命卡（給太太阿毛 2026-05-14 月會用）。
**次要交付物**：10 篇反話術版 Q&A（給阿敦自己學金融商品話術）。

**最大方向翻轉**（2026-05-13）：
- 原定位「金融商品銷售話術 reverse engineering」（客戶視角拆穿話術）
- 翻轉為「理專會議現場救命卡」（理專視角順順答出來）
- 兩個 use case 並存：q01-q10 _\*_.md 給阿敦、aimao-cheatsheet.\* 給阿毛

---

## Timeline

### 2026-05-13

| 時間 | Milestone | 備註 |
|---|---|---|
| 14:00s | 收到截圖三信理專月會 10 題 + ELI20 答案需求 | plan 寫進 `~/.claude/plans/linux-learn-eli20-majestic-spindle.md` |
| 15:14 | mkdir `/mnt/c/Projects/wealth-qa/` 開始 | flat layout、不 git init（initial 用戶選擇）|
| 15:24 | 13 檔（10 篇 q\*.md + README + SOURCES）完成 | 客戶/反話術視角的雙欄拆解（🎤 理專話術版 + 🔍 ELI20 翻譯）|
| 15:33 | WebSearch 跑當期市場數據（14 query）| 補 2026-05 數字進 q\*.md |
| 15:56 | NotebookLM 三方對照 | 發現 NLM 系統性錯誤：Fed funds 5%（實 3.5-3.75%）、降息 78% 機率（實 hold）、SGOV 4.95%（實 3.5%）、MSFT YTD +7.4%（實 -14.5%）、美國 CPI 1.74%（混淆台灣 CPI）等 |
| 16:00 | Perplexity Pro 完整報告對照 | 建 CROSS-CHECK.md：三方準確度 Perplexity > Claude > NotebookLM。S&P 500 YTD 實為 -4.33%（不是 +6% / +7% / +10%）；TAIEX YTD +46%；TSMC 在 0050 60.68%、台股總市值 44-45%、MSCI EM 24.84% |
| 16:03 | **方向翻轉 [reverted]**：阿敦明確「目的是阿毛明天月會」 | 從「反話術文件」翻成「理專救命卡」。產出 aimao-cheatsheet.md / .html。立場 180 度反轉：原本拆穿話術 → 現在順順答話術 |
| 16:06 | HTML cheatsheet 完成 | 響應式手機友善、sticky TOC、淺/暗模式、列印優化 |
| 16:15 | git init + push GitHub | repo `andms9412-debug/wealth-qa` public、Pages 啟用 |
| 16:25 | 阿敦 catch：Q3 0050 個股上限 25% 質疑 | 補充規範分層：主動基金 10% / **台積電條款 25%（2026-04 新規）** / 被動 ETF 無 cap（0050 屬此）/ Capped 版 30% |
| 16:35 | DM PDF 進場（2341.pdf、2448.pdf）| 確認「美事傳富 = 美鴻世代美元分紅（新光）」、「祿得利 = 福祿滿利新台幣 6 年繳（保誠）」。**祿得利是新台幣不是美元（之前假設兩個都是美元錯了）** |
| 16:50 | dark mode 對比度修正 | 阿毛截圖反饋「字超不清楚」→ 加 inline-style box 的 dark mode override CSS |
| 17:00 | Q1 P/E 數字 + MSCI EM Top 4 + YoY 變動 | Q1 30 秒答內嵌權重洗牌敘述（台灣 24.84% > 中國 23.05% > 韓 18.69% > 印度 11.94%）|
| 17:15 | 英式 / 美式 / 澳式分紅比較表 | 補進商品確認段，兩商品都是英式分紅 |
| 17:25 | Q1 改寫家庭主婦白話版 + 保留專業版紅框 | 「打 6 折超市區」比喻 |
| 17:40 | Q2-Q10 全部白話化 | 每題雙語版（白話主版 + 聽眾想聽專業版紅框）|
| 17:45 | 字眼通用化 | 「阿毛 → 讀者」、「主管 → 聽眾」、檔名 aimao-cheatsheet 不變 |

---

## Plan Status

### 完成 ✅

- [x] 10 篇 q\*.md（反話術版，給阿敦學金融商品話術）
- [x] aimao-cheatsheet.md / .html（理專救命卡，給阿毛月會用）
- [x] CROSS-CHECK.md（Claude / NotebookLM / Perplexity 三方對照）
- [x] SOURCES.md（30+ 筆權威來源）
- [x] GitHub Pages live: https://andms9412-debug.github.io/wealth-qa/aimao-cheatsheet.html
- [x] dark mode 對比度修正
- [x] 數據錯誤連環修正（5 個關鍵錯）
- [x] 三信實際商品條款（從 DM）寫入 cheatsheet
- [x] 金管會「台積電條款」（2026-04）規範分層
- [x] 全 Q 白話化 + 字眼通用化

### Pending / 等回饋

- [ ] 阿毛 2026-05-14 月會後 retro：哪些題實戰被點到、答得順不順、有沒有預期外的追問
- [ ] 若阿毛找到更新版商品 DM（如折扣 / 推廣期方案），對應 cheatsheet 更新

### 不做（已決定）

- [x] 不上學術原文 PDF（Vanguard 2012 lump-sum-vs-DCA 等）— 話術強度已夠
- [x] 不做三信 vs 其他銀行通路佣金 / KPI 結構比較 — Tier 5 nice-to-have

---

## Files 索引

| 檔案 | 用途 | 主要讀者 |
|---|---|---|
| `aimao-cheatsheet.md` | 理專月會救命卡（白話 + 專業雙語）| **太太阿毛（核心）** |
| `aimao-cheatsheet.html` | 同上 HTML 版（手機友善 + dark mode）| **太太阿毛（核心）** |
| `q01-em-markets.md` ~ `q10-6040-greed.md` | 10 篇反話術版（雙欄：🎤 理專話術 + 🔍 ELI20 翻譯）| 阿敦學金融商品話術 |
| `q05-products-target.md` / `q06-products-pitch.md` | 兩篇保單題（含 DM 條款）| 阿敦 |
| `q07-1e-bond-fx.md` / `q08-fcn-tech.md` | 進階題（高資產配置 + FCN）| 阿敦 |
| `README.md` | 專案說明 + 2026-05 當期市場 snapshot 表 | 阿敦、未來 fresh session |
| `CROSS-CHECK.md` | Claude WebSearch / NotebookLM / Perplexity 三方對照（含採信規則）| 阿敦驗證數據 |
| `SOURCES.md` | 所有資料來源連結（FRED / iShares / MSCI / 央行 / 三信 cotabank）| 後續更新需要 |
| `PROGRESS.md` | **本檔，SSOT 進度紀錄** | fresh session |

---

## 關鍵 Decisions

### D1：用客戶/投資人視角寫 q\*.md，不用理專視角

- **背景**：原題是「理專該怎麼答客戶」的演練題
- **決定**：q\*.md 寫成「客戶該如何識別話術」的拆穿版（雙欄結構：🎤 理專會這樣答 / 🔍 ELI20 翻譯 / 容易被話術帶走的點 / 你該反問理專的問題）
- **理由**：阿敦不是理專，他要的是「以後遇到推銷能看穿」

### D2：方向翻轉「客戶 → 理專」（核心翻轉）

- **背景**：阿敦中途揭露「實際目的是太太阿毛明天月會被點到能答」
- **決定**：產出第二個交付物 aimao-cheatsheet.\*（理專視角），保留原 q\*.md 並存
- **理由**：兩個 use case 並存，沒衝突

### D3：三方數據採信 Perplexity > Claude > NotebookLM

- **背景**：三方對照後發現 NLM 利率 / yield / 科技股 YTD 系統性偏高（疑用 2024 數據當 2026）
- **決定**：時效類數據以 Perplexity 為主、Claude WebSearch 二次 verify 為輔、NLM 不採用
- **例外**：稅務級距用 Claude 抓的（民國 115 年新版，Perplexity 用舊版）

### D4：cheatsheet 立場「順順答話術」非「拆穿話術」

- **背景**：阿毛是理專，她要賣商品給客戶
- **決定**：cheatsheet 寫「會議現場 30 秒順順答」+「被追問時的精確答」
- **理由**：拆穿話術版對阿毛**有害**（會讓她不敢講 / 穿幫）

### D5：白話版主 + 專業版紅框雙語結構

- **背景**：阿敦回饋「Q2 SGOV / SEC yield 不懂」「Q1 改成家庭主婦版」
- **決定**：每題 30 秒答用白話主版 + 「聽眾想聽專業版」紅框收進專業術語
- **理由**：阿毛現場可選擇「客戶聽得懂」or「主管要聽完整」

### D6：不 commit git config global

- **背景**：阿敦無 global git user config，commit 失敗
- **決定**：用 `git -c user.name=... -c user.email=...` 一次性 override，不寫 global
- **理由**：feedback memory 規則「NEVER update git config」

### D7：GitHub Pages public 部署

- **背景**：阿敦選 public + GitHub Pages（不是 Streamlit、不是私人 Cloud）
- **決定**：repo `andms9412-debug/wealth-qa` public + Pages 從 main / 自動部署
- **理由**：cheatsheet 內容不涉個資、阿毛要手機開 link 最方便

---

## 重大數據錯誤連環修正（學到的教訓）

| 我第一輪寫 | 實際正解 | 來源 |
|---|---|---|
| S&P 500 YTD +7.1% | **-4.33%（total return 5/8）** | Slickcharts |
| MSFT YTD -22.93% | **約 -14.5%** | Yahoo Finance |
| Fed funds 「預期不變、25% 機率升息」（缺全貌）| **3.5-3.75% hold, 2026 預期 hold, 2027 H2 可能升息** | FRED, BofA, JPM |
| LQD yield 4.55% （沒區分 metric）| **30d SEC 5.14% / 12m trailing 4.55%** | iShares |
| F&G Index 66 | **70-76 區間（amsflow 顯示 76 Extreme Greed）** | CNN 不開放 API、第三方差異 |
| 主動基金個股上限 10% | **2026-04 後台積電條款放寬到 25%** | 金管會 |

**教訓**：
1. 30d SEC yield vs 12m trailing yield 是不同 metric，不能混用
2. Total return vs price return 差別在配息
3. 法規可能在 1-2 個月內改變（台積電條款 2026-04 新規）

---

## Self-check（每完成 milestone 跑一次）

當前狀態：
- ☑ 我有 read PROGRESS.md → 本檔剛建立，未來 fresh session 進場必讀
- ☑ 我有 append 新 entry → Timeline 完整收錄
- ☑ 我寫了「進度紀錄類」新檔嗎？→ 沒，PROGRESS.md 本身就是該檔
- ☑ 此次有結論翻轉嗎？→ 有，**D2 方向翻轉**已標 [reverted]
- ☑ Files 段需要加新檔嗎？→ 13 個檔案已收錄
- ☑ Memory 需要 update 嗎？→ 不寫進 memory（PROGRESS.md = SSOT，重複會違反原則）

---

## 下次 fresh session 進來該知道的事

1. **這專案有兩個交付物**：阿毛用 cheatsheet、阿敦學 q\*.md，不要混淆
2. **阿毛 2026-05-14 月會** = 主要 deadline，retro 後可能要 update
3. **三信實際商品已 verify**：美鴻世代（美元）+ 福祿滿利（新台幣），不要再重推測別張
4. **Fed 政策方向**：2026 hold 共識（不是降息也不是升息），下一動作 2027 H2 可能升息
5. **數據時點**：2026-05-13 抓取，**任何超過 7 天的引用都要重新 verify**
6. **GitHub Pages 部署**：https://andms9412-debug.github.io/wealth-qa/aimao-cheatsheet.html

---

**最後更新**：2026-05-13 17:50（initial commit）
