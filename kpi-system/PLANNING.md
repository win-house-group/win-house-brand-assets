# WIN-HOUSE KPI 系統 · 規劃書 (Planning v0.1)

**版本** Version: v0.1 (Draft for Review)
**狀態** Status: Planning · 待 CEO 確認方向
**最後更新** Last Updated: 2026-06-02
**規劃負責人** Owner: Tim Fan, CEO, WIN-HOUSE Group
**設計準則** 遵循 `design-system/SPEC.md` v3.9.14

---

## 0 · 一頁總覽 · Executive Summary

打造一套**自建網頁 App**，讓**業務／PM 每週自助上傳 KPI 資料**，**主管即時追蹤並週匯總**，系統**每月自動匯總產出報表交付 HR**。

| 維度 | 決策 |
|---|---|
| 落地形式 | 自建 Web App，套用 Design System v3.9.14 |
| 使用範圍 | **台灣 + 大陸 雙邊可用**(硬性約束) |
| 帳號基礎 | **Email**(兩岸通用) |
| 通知管道 | 台灣 **LINE** · 大陸 **WeChat/企業微信** · 共用 **Email** |
| 核心節奏 | 業務週上傳 → 主管週追蹤 → 系統月匯總 → HR |
| 角色分層 | 業務 / PM / 主管 / HR / 管理員,**不同職務不同 KPI** |

> ⚠️ **本文件僅為規劃**,尚未開始開發。請 CEO 就「§3 KPI 指標」「§5 流程」「§7 技術選型」確認後,再進入開發路線圖(§9)。

---

## 1 · 系統目標 · Goals

1. **降低業務填報負擔**:每週 5 分鐘內完成上傳,行動裝置可用。
2. **主管即時可視**:不必等月底,週級別就能看到團隊與個人達成率、落後預警。
3. **月匯總自動化**:月底一鍵(或自動排程)產出標準化報表給 HR,免人工貼 Excel。
4. **職務差異化**:業務、PM、主管各有專屬指標與權重,公平且可比較。
5. **兩岸無痛使用**:台灣與大陸同仁體驗一致、連線穩定、通知到位。

### 非目標 · Non-Goals(本期不做)
- 不做薪酬/獎金自動計算(僅提供 HR 匯總數據,計薪仍由 HR 主導)。
- 不做 ERP / CRM 取代(可串接,但本期以**手動上傳 + 選擇性匯入**為主)。
- 不做客戶端對外功能(純內部工具)。

---

## 2 · 角色與權限 · Roles & Permissions

| 角色 | 主要動作 | 可見範圍 |
|---|---|---|
| **業務 Sales** | 每週上傳個人 KPI 資料、查看個人儀表板 | 僅本人 |
| **PM** | 每週上傳產品線 KPI、查看個人儀表板 | 僅本人 + 其負責產品線 |
| **主管 Manager** | 追蹤部屬週報、審核/退回、週匯總、加註解 | 本部門全員 |
| **HR** | 接收月匯總報表、匯出 | 全公司彙總(唯讀,不可改原始資料) |
| **管理員 Admin** | 設定 KPI 指標/權重/目標值、帳號與部門、排程 | 全系統設定 |

**權限原則**(對齊資安最小化):
- 業務看不到別人的數字;主管只看自己團隊;HR 只拿到匯總層,不碰逐筆原始輸入。
- 目標值(Target)只有主管/Admin 可設定,業務只能填實際值(Actual),避免自評灌水。

---

## 3 · KPI 指標設計 · KPI Catalog(★ 核心)

> 本表為**建議版**,數字權重可在 Admin 後台調整。WIN-HOUSE 為代理/分銷型態(「Your Best Partner」、原廠 co-brand),故 **PM = 產品線/原廠線 Product Manager**,KPI 以產品線經營為核心。

### 3.1 業務 Sales(權重合計 100%)

| # | 指標 | 定義/公式 | 建議權重 | 上傳頻率 | 方向 |
|---|---|---|---|---|---|
| S1 | 業績達成率 | 當期實際營收 ÷ 目標營收 | 30% | 週 | ↑ 越高越好 |
| S2 | 毛利達成率 | 實際毛利 ÷ 目標毛利 | 20% | 週 | ↑ |
| S3 | 新客戶開發 | 新成交/新開發客戶數 | 10% | 週 | ↑ |
| S4 | 報價轉換率 | 成交筆數 ÷ 報價筆數 | 10% | 週 | ↑ |
| S5 | Pipeline 金額 | 進行中商機加權金額 | 10% | 週 | ↑ |
| S6 | 客戶拜訪/有效接觸 | 拜訪或線上有效接觸次數 | 5% | 週 | ↑ |
| S7 | 送樣/樣品申請 | 送樣件數(代理業關鍵前導指標) | 5% | 週 | ↑ |
| S8 | 應收帳款帳齡 | 逾期 AR 金額 / 平均收款天數 DSO | 10% | 週 | ↓ 越低越好 |

### 3.2 PM 產品經理(權重合計 100%)

| # | 指標 | 定義/公式 | 建議權重 | 上傳頻率 | 方向 |
|---|---|---|---|---|---|
| P1 | 產品線營收達成 | 產品線實際營收 ÷ 目標 | 25% | 週/月 | ↑ |
| P2 | 產品線毛利率 | 產品線毛利 ÷ 營收 | 20% | 月 | ↑ |
| P3 | Design-in / Design-win | 導入/設計勝出案數 | 15% | 週 | ↑ |
| P4 | 新產品/新料號導入 | 新上架 SKU 或新原廠線 | 10% | 月 | ↑ |
| P5 | 庫存周轉率 | 營業成本 ÷ 平均庫存 | 10% | 月 | ↑ |
| P6 | 呆滯庫存 (E&O) | 呆滯/超齡庫存金額占比 | 10% | 月 | ↓ |
| P7 | 預測準確率 | 1 −|預測−實際|÷ 實際 | 5% | 月 | ↑ |
| P8 | 原廠關係/教育訓練 | 原廠拜訪、訓練場次、聯合活動 | 5% | 月 | ↑ |

### 3.3 主管 Manager(管理型 KPI,權重合計 100%)

| # | 指標 | 定義/公式 | 建議權重 | 方向 |
|---|---|---|---|---|
| M1 | 團隊整體達成率 | 團隊實際 ÷ 團隊目標 | 40% | ↑ |
| M2 | 人均產值 | 團隊營收 ÷ 團隊人數 | 20% | ↑ |
| M3 | 部屬週報繳交率 | 準時繳交人次 ÷ 應繳人次 | 15% | ↑ |
| M4 | 預測 vs 實際偏差 | 月初承諾 vs 月底實際 | 15% | ↓(偏差越小越好) |
| M5 | 人員留任/培育 | 留任率、晉升/輔導達成 | 10% | ↑ |

### 3.4 評分與燈號 · Scoring

- **單項得分** = `min(實際/目標, 上限) × 100`(↓向指標反向計算)。
- **綜合 KPI 分** = `Σ(單項得分 × 權重)`。
- **燈號**(對齊 Design System Semantic Colors):
  - 🟢 達標 ≥ 100% → `--success` / Data Green `#5D8722`
  - 🟡 接近 80–99% → Data Gold `#DF9C41`(預警)
  - 🔴 落後 < 80% → Data Rust `#923621`(需主管介入)

---

## 4 · 資料模型 · Data Model

核心資料表(Web App 後端):

```
users        : id, name, email, role(sales/pm/manager/hr/admin),
               dept_id, region(TW/CN), locale, im_channel(line/wechat), active
departments  : id, name, manager_id, parent_id
kpi_defs     : id, role, code(S1..), name_zh, formula, unit,
               direction(up/down), weight, frequency(week/month)
kpi_targets  : id, user_id, kpi_def_id, period(YYYY-Wnn / YYYY-MM), target_value
kpi_entries  : id, user_id, kpi_def_id, period, actual_value,
               status(draft/submitted/approved/returned),
               submitted_at, note, attachment_url
review_logs  : id, entry_id, reviewer_id, action, comment, created_at
periods      : id, type(week/month), code, start_date, end_date, locked
audit_logs   : id, user_id, action, target, created_at   # 資安稽核
```

**設計重點**
- 一筆 `kpi_entry` = 某人某指標某期間的實際值,主管審核狀態機:`draft → submitted → approved / returned`。
- `kpi_targets` 與 `kpi_entries` 分離 → 目標由主管設、實際由業務填,責任清楚。
- `period.locked` 月鎖檔:HR 取數後鎖定,避免事後竄改(資安/稽核需求)。

---

## 5 · 核心流程 · Workflows

### 5.1 週流程(業務/PM)
```
週一  系統推播提醒(LINE/WeChat/Email):本週尚未填報
週間  業務隨時上傳實際值(手機/電腦),可存草稿
週五 17:00  截止提醒;未交者再推一次
週五截止後  狀態鎖為待審
```

### 5.2 週流程(主管)
```
主管儀表板看到團隊紅黃綠燈 + 繳交率
逐筆審核 → 核准 / 退回(附退回理由)
對落後(紅燈)業務加註追蹤行動
產出「週匯總快照」(自動,可加主管評語)
```

### 5.3 月流程(系統 → HR)
```
每月最後工作日 23:00 排程:
  1. 彙總當月各角色 KPI 綜合分與達成率
  2. 套用 Design System 產出標準報表(線上 Dashboard + 可匯出 PDF/Excel)
  3. 鎖檔該月期間(period.locked = true)
  4. 推播通知 HR + 主管:本月匯總已就緒
HR 登入唯讀檢視、匯出,送薪酬/績效流程
```

### 5.4 狀態機 · State Machine
```
[草稿 draft] --submit--> [待審 submitted] --approve--> [核准 approved]
                                       \--return--> [退回 returned] --resubmit--> [待審]
月底鎖檔: approved 之外的逾期項標記為「未繳/缺漏」一併呈現給主管與 HR
```

---

## 6 · Dashboard 設計 · UI(套用 Design System v3.9.14)

| 角色 | 預設首頁 |
|---|---|
| 業務/PM | 個人本週填報卡 + 個人達成率趨勢 + 紅黃綠燈 |
| 主管 | 團隊熱力表(人 × 指標燈號)+ 繳交率 + 待審清單 |
| HR | 月匯總:部門/角色比較、達成率分布、可匯出 |

**視覺準則**(摘自 SPEC.md):
- 黑白灰為主(80%+),資料區塊用 `--surface-1 #F5F5F5`,**避免全黑表格底**。
- 圖表用色「少即是多」,單 Dashboard 4–5 色:
  - 達成率排序 → **暖系漸層** `--data-gold-light → --data-rust`(策略 A)
  - 成長 vs 衰退 → **暖冷雙軸**(策略 B)
  - 凸顯落後個案 → **對比強調 1 色 + 灰階**(策略 C)
- KPI 燈號用 Semantic 三色(綠/金/鏽)。
- Logo Red `#E1251B` 僅用於 Logo,不可當圖表色。
- Empty State / 達標慶祝可放 WINGO(`wingo/wingo-hi.png`),符合內部工具場景。

---

## 7 · 技術選型 · Architecture(★ 兩岸可用為硬約束)

### 7.1 鐵律:大陸防火牆相容
| 禁用(大陸會被擋/不穩) | 改用 |
|---|---|
| Google Fonts / Firebase / Google APIs | **自架字型**(Noto Sans TC/SC 自 host) |
| Google 登入 / reCAPTCHA | **Email 帳密 + Email 驗證碼/Magic Link** |
| 部分海外 CDN(含 jsDelivr 偶不穩) | 靜態資產**自架** + 兩岸可達 CDN |
| 純海外單機房 | **就近節點 / 多區部署** |

### 7.2 建議架構
- **前端**:單頁式 App(Vue 3 或 React),響應式(手機優先,業務多在外),套 Design System tokens。
- **後端**:Node.js (NestJS) 或 Python (FastAPI);REST API。
- **資料庫**:PostgreSQL(或 MySQL);物件儲存放附件。
- **部署**:
  - 方案 A(推薦,務實):主機放**香港/新加坡節點**(阿里雲/AWS),兩岸皆可達;靜態資產走兩岸可達 CDN。免大陸 ICP 備案,最快上線。
  - 方案 B(規模大時):大陸 + 海外**雙區部署**,大陸節點需辦 **ICP 備案**,合規最佳但工期長。
  - → **本期建議 A**,日後量大再升級 B。
- **帳號/驗證**:Email 為主鍵;Magic Link 或 Email OTP 登入(免記密碼、兩岸通用)。
- **通知服務**(抽象成一層 `notifier`,依 region 路由):
  - 台灣 → LINE Messaging API / LINE Notify
  - 大陸 → 企業微信 (WeChat Work) 應用消息
  - 共用保底 → Email(SMTP)
- **i18n**:介面繁中/簡中切換(`users.locale`)。

### 7.3 資安與合規
- 全程 HTTPS;密碼/OTP 不落明碼;附件存取簽名 URL。
- `audit_logs` 全操作留痕;月底 `period.locked` 防竄改。
- 角色最小權限;HR 唯讀匯總層。
- 兩岸個資:資料分級,跨境傳輸留意大陸個資法(PIPL)/台灣個資法,匯出報表去識別化選項。

---

## 8 · 與現有資產整合 · Integration

- **品牌**:沿用 `design-system/SPEC.md` tokens 與 `wingo/` 吉祥物;新增 KPI 專用 chart 樣式可回饋進 design-system。
- **CDN 引用**:README 既有 jsDelivr 引用方式適用於對外素材;但**系統內部靜態資產建議自架**以確保大陸連線(見 §7.1)。
- **LINE 自動週報**:README 已列「LINE 自動週報」為適用場景,正好對接本系統 §5 的週推播。

---

## 9 · 開發路線圖 · Roadmap(待方向確認後啟動)

| 階段 | 內容 | 產出 | 預估 |
|---|---|---|---|
| **P0 確認** | CEO 確認 KPI 指標/權重、流程、選型 | 定版規劃書 | 本週 |
| **P1 MVP** | Email 登入、業務週上傳、主管審核、個人/團隊儀表板 | 可內部試用 | 2–3 週 |
| **P2 匯總** | 月排程匯總、HR 唯讀報表、PDF/Excel 匯出、鎖檔 | HR 可用 | +2 週 |
| **P3 通知** | LINE / WeChat / Email 推播、繁簡 i18n | 兩岸全通 | +1–2 週 |
| **P4 強化** | ERP/CRM 選擇性匯入、權重模擬、稽核強化 | 正式上線 | 視需求 |

**先導試點**:建議先挑 1 個業務團隊 + 1 條 PM 產品線跑 P1,兩週後校正指標與權重再全面推。

---

## 10 · 待 CEO 決策清單 · Open Questions

1. **§3 KPI 指標與權重**是否符合公司實際?(尤其 PM 是否為「產品線經理」定位)
2. **目標值來源**:由主管手動設,或從 ERP/年度預算匯入?
3. **匯總頻率**:HR 只要月報,或也要季/年報?
4. **試點範圍**:先從哪個團隊/產品線開始?
5. **部署方案** A(港星節點,快)或 B(大陸備案,合規)?
6. 是否要**獎金試算**(本期列 Non-Goal,可改列入)?

---

© WIN-HOUSE Group · 文浩集團 · Since 1987 · KPI System Planning v0.1
