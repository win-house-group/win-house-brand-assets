# Win-House Brand Assets

文浩集團對外公開品牌資產儲存庫。本 Repo 透過 **GitHub Pages** 服務,可供 AI 工具、簡報、文件、網站直接引用。

> **權威設計規範(有衝突以它為準):**
> 互動版 → https://win-house-group.github.io/winhouse-brand-assets/design-system/
> 完整 SPEC → https://win-house-group.github.io/winhouse-brand-assets/design-system/SPEC.md

---

## 🆕 v3.14.0 重點(2026-06-28)

1. **網域已遷移**:資產主機從舊帳號 `timfan119`(jsDelivr / GitHub-raw)改到 GitHub Pages 組織網域 `win-house-group.github.io`。舊連結一律停用,不再產生。
2. **新增反白 Logo**:`Win-House-Group-wt.png`(白字,深色底專用)。
3. **快取簡化**:Pages 直接服務最新 commit,**不需** jsDelivr 的 `?v=N` 破解或 `purge.jsdelivr.net`(已退役)。瀏覽器看到舊圖時,才在連結後加 `?v=N`。

---

## 📦 資產目錄

| 路徑 | 內容 | 狀態 |
|---|---|---|
| `/Win-House-Group-bk.png` | 完整商標(黑字,淺底用) | Active |
| `/Win-House-Group-wt.png` | 完整商標(白字,深底用)🆕 | Active |
| `/winhouse-logo-red.png` | 純識別標誌(紅色 Mark) | Active |
| `/wingo/` | WINGO 吉祥物姿態與表情 | Active |
| `/design-system/` | 互動規範頁 + `SPEC.md` + `winhouse-tokens.css` | Active |

---

## 🔗 資產正式 URL(只用這些)

基礎網域:`https://win-house-group.github.io/winhouse-brand-assets/`

| 資產 | 直接連結 |
|---|---|
| Logo 完整商標(黑,**淺底**用) | `https://win-house-group.github.io/winhouse-brand-assets/Win-House-Group-bk.png` |
| Logo 完整商標(白,**深底**用)🆕 | `https://win-house-group.github.io/winhouse-brand-assets/Win-House-Group-wt.png` |
| Logo 純識別標誌(紅 Mark) | `https://win-house-group.github.io/winhouse-brand-assets/winhouse-logo-red.png` |
| WINGO 揮手打招呼 | `https://win-house-group.github.io/winhouse-brand-assets/wingo/wingo-hi.png` |
| Design Tokens CSS | `https://win-house-group.github.io/winhouse-brand-assets/design-system/winhouse-tokens.css` |
| 完整規範 SPEC.md | `https://win-house-group.github.io/winhouse-brand-assets/design-system/SPEC.md` |

> **Logo 配對鐵則**:淺底 → 黑版 `-bk`;深底 → 白版 `-wt`。**禁止手動改色**;黑 Logo 不可放深底,白 Logo 不可放淺底。

---

## 🤖 在 AI 對話中引用

把以下整段貼到任何 AI 對話視窗,讓它先讀規範再產出:

> 我是 Win-House 集團(文浩集團)CEO Tim Fan。
> 產出任何 Win-House 視覺/前端素材前,請先讀取我們的 Design System v3.14.0:
> https://win-house-group.github.io/winhouse-brand-assets/design-system/SPEC.md
>
> 核心約束(不可違反):
> - 唯一受保護品牌色 Logo Red #E1251B,僅限 Logo,絕不當 UI 底色。
> - 黑白灰為主視覺(80%+);金 #DF9C41 是點綴/強調,不是預設鋪色。
> - 字體:標題 Antonio、繁中 Noto Sans TC、簡中 Noto Sans SC、UI/料號 Inter。
> - HTML 輸出請先連 tokens:https://win-house-group.github.io/winhouse-brand-assets/design-system/winhouse-tokens.css
> - 圖表務必照 SPEC 的 Chart Gallery STRICT 規範(先選圖決策樹 → 套硬規則 → 出圖前自檢)。
>
> 吉祥物 WINGO(白頭海鵰、黑西裝、紅領帶、胸前 WH 紅標)圖檔:
> https://win-house-group.github.io/winhouse-brand-assets/wingo/wingo-hi.png

---

## 🎨 品牌色票(v3.14.0 — 舊五色已廢止)

> ⚠️ 舊版品牌五色(Gold `#C9941F` / Slate Blue `#4A6B8A` / Clay `#B57258` / Sage `#5A8159`)自 v3.9.6 起**全部廢止**,改用下方系統。請勿再使用。

**受保護品牌色(唯一)**

| Token | HEX | 用途 |
|---|---|---|
| Logo Red | `#E1251B` | 僅限 Logo,絕不作 UI 底色或語意色 |

**表面色 Surfaces**

| Token | HEX |
|---|---|
| `--bg` | `#FFFFFF` |
| `--page-bg` | `#F4F4F3` |
| `--surface-1` | `#F5F5F5` |
| `--surface-2` | `#FAFAFA` |
| `--text-1` | `#1A1A1A` |
| `--text-2` | `#737373` |
| `--border` | `#E5E5E5` |
| Hero 深底(僅 Hero) | `#0A0A0A` |

**Data Palette(9 色,圖表/強調用)**

| Token | HEX |
|---|---|
| gold-light | `#E4AF79` |
| gold | `#DF9C41` |
| bronze | `#AF7231` |
| rust | `#923621` |
| charcoal | `#2D2A28` |
| blue-deep | `#2677A5` |
| blue-light | `#639BC1` |
| olive | `#90A74A` |
| green | `#5D8722` |

**語意色 Semantic(西方慣例)**

| 用途 | HEX | Token |
|---|---|---|
| 漲 / 成長 | `#5D8722` | `--sem-up` |
| 跌 / 衰退 | `#C9302C` | `--sem-down` |
| 警示 / 注意 | `#DF9C41` | `--sem-warn` |

---

## 📊 圖表規範(STRICT — 最常被忽略)

完整規則見 SPEC.md。重點:

1. **先答「這張圖回答哪個問題」再選圖種**:變好壞(≤11 期)→ 直條;長期(≥12 期)→ 折線;排名 → 橫條;占比(≤5 類)→ 圓環;兩群比較 → 雙組直條。
2. 一圖一色族;單頁 ≤5 色;金色只塗那一個重點,其餘灰階。
3. 禁 3D / 漸層光暈 / 動畫 / emoji 資料點;數字 ≥28px,不縮字塞內容。
4. 語意色(漲跌警示)/ 領域色(僅占比結構圖分類)/ 單色族深淺(同類比大小)**三者不可互換**。
5. 出圖前跑 SPEC 的 9 項自檢,全過才出圖。

---

## ⚖️ WINGO 使用規範

### ✅ 適用場景
- 內部工具(職級地圖、KPI Dashboard 的 empty-state / loading / success / level-up)
- LINE 自動週報封面
- 內部訓練教材與簡報內頁
- 系統提示頁、官網軟性頁、LinkedIn 軟性貼文

### ❌ 排除場景
- 官網首頁 Hero 與產品型錄
- Datasheet 與原廠技術文件
- 報價單、契約、發票
- Tier 1 客戶提案封面
- 原廠 Co-branded 行銷素材
- 大紅底色塊

> 原則:親切 → 上場;專業 → 收斂;員工看的 → 適合;客戶 & 硬性業務 → 不用。
> 在合適場景產生素材前,先確認是否要讓 WINGO 出場,不擅自加入。

---

## 🏢 公司正式名稱(對外文件)

- 台灣:文浩實業有限公司 / WIN-HOUSE CO., LTD.
- 香港:文浩國際(香港)有限公司 / WIN-HOUSE INTERNATIONAL (H.K.) LTD.
- 越南:文浩國際(越南)有限公司 / WIN-HOUSE INTERNATIONAL (VIETNAM) LTD.
- 深圳:深圳市宇宙光電子有限公司 / SHENZHEN UNIVERSE LIGHT ELECTRONIC CO., LTD.

> 單一主品牌 `Win-House Group`;不採用 `TDK × WIN-HOUSE` 共同品牌鎖定。Tagline:`Your best partner!` / 「樂觀進取」。

---

## 📝 版本紀錄

| 日期 | 版本 | 更新 |
|---|---|---|
| 2026-06-28 | v3.14.0 | 網域遷移至 GitHub Pages 組織域 `win-house-group.github.io`;新增反白 Logo `Win-House-Group-wt.png`;jsDelivr 快取破解退役;README 全面更新(舊五色廢止、加入 Design System / 圖表規範)。 |
| 2026-05-26 | v0.1 | 初次發佈,加入 WINGO Greeting (Hi)。 |

---

© Win-House Group · 文浩集團 · Since 1987
