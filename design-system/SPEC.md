# WIN-HOUSE Design System v3.10.0 · Official Specification

**版本** Version: v3.10.0 (Production)
**狀態** Status: Active · Mandatory
**最後更新** Last Updated: 2026-05-26
**規範負責人** Owner: Tim Fan, CEO, WIN-HOUSE Group

---

## ⚠️ 強制聲明 · MANDATORY NOTICE · 强制声明

**[繁中]** 本規範為文浩集團統一視覺準則,適用於所有 frontend 介面、內部工具、對外網站、簡報範本、AI 生成素材與跨語系頁面。任何 AI、設計師、外包合作夥伴產出 Win-House 視覺素材前,**必須先讀取本規範**並嚴格遵循。本文件取代過往所有版本(v2、v3.0–v3.9.14 全部廢止)。

**[English]** This specification is the unified visual standard for WIN-HOUSE Group, applicable to all frontend interfaces, internal tools, external websites, presentation templates, AI-generated assets, and multi-language pages. Any AI, designer, or third-party partner producing visual materials for WIN-HOUSE **must read this specification first** and follow it strictly. This document supersedes all previous versions (v2, v3.0–v3.9.14 are deprecated).

**[简中]** 本规范为文浩集团统一视觉准则,适用于所有 frontend 界面、内部工具、对外网站、演示模板、AI 生成素材与跨语种页面。任何 AI、设计师、外包合作伙伴产出 Win-House 视觉素材前,**必须先读取本规范**并严格遵循。本文件取代过往所有版本(v2、v3.0–v3.9.14 全部废止)。

---

## 📐 01 · Color Tokens · 配色 · 配色

### 🎯 v3.9.7 配色系統哲學 · Color System Philosophy

**[繁中]** v3.9.6 起,Win-House 配色精簡為**單一品牌識別色 + Data Palette 9 色擴展 + Semantic 3 色 + 應用領域對應**四層結構。原品牌五色(Gold / Slate Blue / Clay / Sage)全部廢止,改由 Data Palette 對應取代。**黑白灰仍為主視覺(佔比 80%+)**。

**[English]** From v3.9.6, Win-House colors are restructured into four layers: **single brand identity + Data Palette 9-color extension + Semantic Colors 3-set + Application Domain Mapping**. The original 5 brand colors (Gold / Slate Blue / Clay / Sage) are deprecated and replaced by Data Palette equivalents. **Black/white/gray remain dominant (80%+).**

**[简中]** v3.9.6 起,Win-House 配色精简为**单一品牌识别色 + Data Palette 9 色扩展 + Semantic 3 色 + 应用领域对应**四层结构。原品牌五色(Gold / Slate Blue / Clay / Sage)全部废止,改由 Data Palette 对应取代。**黑白灰仍为主视觉(占比 80%+)**。

### 📝 Text & Background Rules · 文字與底色原則 · 文字与底色原则 (v3.10.0)

**[繁中]**
- 文字以**黑、灰為主**(`--text-1` / `--text-2`)。
- **白字僅用於深底色**(Hero、深色按鈕、實心標籤);若搭配底色,需確保對比充足。
- **一般白底時禁用藍色字**——藍色僅作為色塊填充、邊框,或出現在深底色上。
- 小型文字(標籤、token 名)若用金色,使用**深金 `--gold-hover` #AF7231**(非亮金 #DF9C41),確保白底可讀性。
- **表格、資料區塊避免全黑為底**(太重);使用淺色表面 `--surface-1`,黑底僅保留給 Hero。

**[English]**
- Text is primarily **black and gray** (`--text-1` / `--text-2`).
- **White text only on dark backgrounds** (Hero, dark buttons, solid tags); ensure sufficient contrast when paired with color.
- **No blue text on plain white backgrounds** — blue only as fill, border, or on dark surfaces.
- For small text in gold, use **deep gold `--gold-hover` #AF7231** (not bright #DF9C41) for white-background legibility.
- **Avoid full-black backgrounds for tables/data blocks** (too heavy); use light `--surface-1`, reserve black for Hero only.

**[简中]**
- 文字以**黑、灰为主**(`--text-1` / `--text-2`)。
- **白字仅用于深底色**(Hero、深色按钮、实心标签);若搭配底色,需确保对比充足。
- **一般白底时禁用蓝色字**——蓝色仅作为色块填充、边框,或出现在深底色上。
- 小型文字(标签、token 名)若用金色,使用**深金 `--gold-hover` #AF7231**(非亮金 #DF9C41),确保白底可读性。
- **表格、数据区块避免全黑为底**(太重);使用浅色表面 `--surface-1`,黑底仅保留给 Hero。

### Core Brand · 核心品牌色(單一)

| Token | HEX | Role |
|---|---|---|
| `--logo-red` | `#E1251B` | Logo only · 僅 Logo · 仅 Logo (業績長紅意象) |

### Surfaces · 表面色

| Token | HEX | Role |
|---|---|---|
| `--page-bg` | `#F4F4F3` | **Page background (v3.10)** · 頁面底(微暖淺灰) |
| `--bg` | `#FFFFFF` | Card / content background · 卡片與內容底 |
| `--surface-1` | `#F5F5F5` | In-card secondary surface · 卡內次層(表頭、標籤底) |
| `--surface-2` | `#FAFAFA` | In-card tertiary surface · 卡內三層(輸入框底) |
| `--text-1` | `#1A1A1A` | Primary text · 主文字 |
| `--text-2` | `#737373` | Secondary text · 次文字 |
| `--text-3` | `#A3A3A3` | Tertiary text · 輔助文字 |
| `--border` | `#E5E5E5` | Divider / table border · 分隔線與表格線 |
| `--card-border` | `#ECECEA` | **Card border (v3.10)** · 卡片柔邊框 |
| `--hero-bg` | `#0A0A0A` | Hero showcase only · Hero 展示專用 |

### 🪶 Elevation & Surface System · 層次系統 (v3.10)

**[繁中]** v3.10 起,層次手法從「白頁面 + 灰卡片(邊框分層)」反轉為「**淺灰頁面 + 白卡片(柔陰影分層)**」。三層結構:頁面底 `--page-bg` #F4F4F3(微暖淺灰)> 白色卡片 + `--shadow-card` 柔陰影 + `--card-border` 柔邊框 > 卡內淺灰次層(`--surface-1/2`)。陰影使用微暖黑 `rgba(28,25,20,…)` 取代純黑,更柔和自然。**色相完全不變**——黑白灰 80%、金 20%、Data Palette 與語意色均維持 v3.9.6 鎖定值;改變的只有表面處理質感。Hero 黑底保留並加 `--shadow-elevated` 懸浮。

**[English]** From v3.10, the elevation method inverts from "white page + gray cards (border-separated)" to "**light-gray page + white cards (soft-shadow-separated)**". Three layers: page `--page-bg` #F4F4F3 (warm-tinted light gray) > white cards with `--shadow-card` and `--card-border` > in-card light-gray sub-surfaces (`--surface-1/2`). Shadows use warm black `rgba(28,25,20,…)` instead of pure black for a softer feel. **Hue is fully unchanged** — black/white/gray 80%, gold 20%, Data Palette and semantic colors all keep their v3.9.6 locked values; only the surface treatment changes. The black Hero stays, elevated with `--shadow-elevated`.

**[简中]** v3.10 起,层次手法从「白页面 + 灰卡片(边框分层)」反转为「**浅灰页面 + 白卡片(柔阴影分层)**」。三层结构:页面底 `--page-bg` #F4F4F3 > 白色卡片 + 柔阴影 + 柔边框 > 卡内浅灰次层。阴影使用微暖黑 `rgba(28,25,20,…)`。**色相完全不变**——黑白灰 80%、金 20%、Data Palette 与语义色均维持 v3.9.6 锁定值;改变的只有表面处理质感。Hero 黑底保留并加悬浮阴影。

| Shadow Token | Value |
|---|---|
| `--shadow-card` | `0 1px 2px rgba(28,25,20,0.03), 0 10px 30px rgba(28,25,20,0.06)` |
| `--shadow-elevated` | `0 2px 6px rgba(28,25,20,0.05), 0 20px 48px rgba(28,25,20,0.10)` |

### Data Palette · 數據視覺化專用 · 数据可视化专用

**[繁中]** 取自 Charles Demuth《I Saw the Figure 5 in Gold》(暖金土系)與 Richard Diebenkorn《Seawall》(冷藍綠系),9 色擴展。**用於 Chart / Dashboard / 數據視覺化,以及一般強調用色**(取代原品牌五色)。

**[English]** Inspired by Charles Demuth's *I Saw the Figure 5 in Gold* (warm earth) and Richard Diebenkorn's *Seawall* (cool blue-greens). 9-color extension **for charts, dashboards, data visualization, and general accent usage** (replaces the old 5 brand colors).

**[简中]** 取自 Charles Demuth《I Saw the Figure 5 in Gold》(暖金土系)与 Richard Diebenkorn《Seawall》(冷蓝绿系),9 色扩展。**用于 Chart / Dashboard / 数据可视化,以及一般强调用色**(取代原品牌五色)。

**色塊分組(以接近色排列)· Color Grouping (by adjacency)**:

| Group · 組別 | Tokens | Range |
|---|---|---|
| 暖系 · Warm | `--data-gold-light` `--data-gold` `--data-bronze` `--data-rust` | #E4AF79 → #923621 |
| 冷系 · Cool | `--data-blue-deep` `--data-blue-light` `--data-olive` `--data-green` | #2677A5 → #5D8722 |
| 中性 · Neutral | `--data-charcoal` | #2D2A28 |

| Token | HEX | Category | Replaces |
|---|---|---|---|
| `--data-gold-light` | `#E4AF79` | Warm 01 · 暖系 | — |
| `--data-gold` | `#DF9C41` | Warm 02 | old `--gold` #C9941F |
| `--data-bronze` | `#AF7231` | Warm 03 | old `--gold-hover` |
| `--data-rust` | `#923621` | Warm 04 | old `--clay` #B57258 |
| `--data-blue-deep` | `#2677A5` | Cool 01 · 冷系 | old `--slate-blue` #4A6B8A |
| `--data-blue-light` | `#639BC1` | Cool 02 | — |
| `--data-olive` | `#90A74A` | Cool 03 | — |
| `--data-green` | `#5D8722` | Cool 04 | old `--success` #5A8159 |
| `--data-charcoal` | `#2D2A28` | Neutral · 中性 | Do/Don't Negative |

### Dashboard Color Strategies · 圖表用色策略 · 图表用色策略

**[繁中]** 圖表用色「**少即是多**」。一般 Dashboard 建議單次使用 4-5 色,而非全部 9 色。提供三種推薦策略:

**[English]** For charts, **less is more**. Use 4-5 colors per dashboard, not all 9. Three recommended strategies:

**[简中]** 图表用色「**少即是多**」。一般 Dashboard 建议单次使用 4-5 色,而非全部 9 色。提供三种推荐策略:

| Strategy · 策略 | Use Case · 適用情境 | Colors Recommended |
|---|---|---|
| **A · Same-family Gradient** 同色族漸層 | Degree of difference · 程度差異(庫存等級、業績區間) | Warm 4 連 OR Cool 4 連 |
| **B · Warm-Cool Dual Axis** 暖冷雙軸 | Two-category contrast · 兩類別對比(成長 vs 衰退) | 2 暖 + 2 冷 |
| **C · Contrast Emphasis** 對比強調 | Highlight key data · 凸顯重點 | 1 強調色 + 灰階配角(#E5E5E5) |

**Recommended ordering**: For sequential data, use Warm gradient (Gold Light → Rust) or Cool gradient (Blue Deep → Green). For categorical data, alternate between warm and cool groups.

### Semantic Colors · 語意配色 · 语义配色

For Stat Delta and KPI direction indicators (up/down/warn):

| Token | HEX | Semantic |
|---|---|---|
| `--tw-red` | `#C9302C` | UP · 上漲 · 上涨 |
| `--tw-green` | `#5D8722` | DOWN · 下跌 · 下跌 |
| `--tw-yellow` | `#DF9C41` | WARN · 警示 · 警示 |

> Color logic follows Greater-China market convention. Token naming uses `tw-*` prefix for clarity but applies to any locale where red=up / green=down is expected.

### Application Domain Color Mapping · 應用領域配色 · 应用领域配色

**[繁中]** 從 Data Palette 中,依照各應用領域的「市場慣用色 / 物理意象」對應到最適配的顏色。此對應為 **Win-House 內部產業圖表的標準色映射**,適用於業績分布、應用占比、客戶結構等視覺化場景。

**[English]** Maps each application domain to its most fitting color from the Data Palette, based on industry conventions and physical imagery. This is the **standard for Win-House industry-related charts** — revenue distribution, application share, client structure visualizations.

**[简中]** 从 Data Palette 中,依照各应用领域的「市场惯用色 / 物理意象」对应到最适配的颜色。此对应为 **Win-House 内部产业图表的标准色映射**。

| Domain · 領域 · 领域 | HEX | Token | Rationale · 理由 |
|---|---|---|---|
| Optical · 光通訊 · 光通讯 | `#E4AF79` | `--data-gold-light` | Warm light imagery · 光的暖白意象 |
| Automotive · 汽車 · 汽车 | `#2677A5` | `--data-blue-deep` | Auto IC industry blue · 車用 IC 慣用深藍 |
| Networking · 網通 · 网通 | `#639BC1` | `--data-blue-light` | Cisco-tier blue · Cisco 系藍綠 |
| Industrial · 工業 · 工业 | `#AF7231` | `--data-bronze` | Bronze metal feel · 銅棕金屬感 |
| Power · 電源 · 电源 | `#923621` | `--data-rust` | High-voltage rust · 高壓警示鐵鏽 |
| Consumer · 消費電子 · 消费电子 | `#DF9C41` | `--data-gold` | Warm lifestyle gold · 暖金生活感 |
| Robotics · 機器人 · 机器人 | `#2D2A28` | `--data-charcoal` | Mechanical charcoal · 機械炭黑 |
| Drone · 無人機 · 无人机 | `#90A74A` | `--data-olive` | Military olive · 軍規橄欖綠 |
| AR / Satellite · AR / 衛星 | `#5D8722` | `--data-green` | Deep vision green · 深綠視野 |

**Usage Note · 使用注意**:
- For new application domains not listed above, propose a mapping based on industry convention or physical imagery, and add to this table.
- 新增應用領域時,依照市場慣用色或物理意象建議對應顏色,並更新此表。
- 新增应用领域时,依照市场惯用色或物理意象建议对应颜色,并更新此表。

### ⚠️ Bipolar Accent v2 · 雙極對比制 v2

The Bipolar Accent pattern is updated in v3.9.6:

| Context | Positive · 正向 | Negative · 負向 |
|---|---|---|
| **Stat Delta** | `--tw-red` #C9302C (UP) | `--tw-green` #5D8722 (DOWN) |
| **Stat Delta · Warning** | `--tw-yellow` #DF9C41 (WARN/LOW) | — |
| **Do / Don't** | `--tw-red` #C9302C border | `--data-charcoal` #2D2A28 border |
| **WINGO Decision** | `--tw-red` (warmth/use · 親切/上場) | `--data-charcoal` (premium/hold · 專業/收斂) |

---

## ✍️ 02 · Typography · 字體 · 字体

**四套字體分工 · Four-Font System · 四套字体分工**

| Font Family | Source | Usage · 用途 · 用途 |
|---|---|---|
| **Antonio** | Google Fonts | **Headings & brand emphasis ONLY** · 僅標題與品牌強調 · 仅标题与品牌强调 (Display, Section Title, Hero, Logo) |
| **Noto Sans TC** | Google Fonts | Traditional Chinese + numerals · 繁體中文 + 一般數字 · 繁体中文 + 一般数字 |
| **Noto Sans SC** | Google Fonts | Simplified Chinese + numerals · 簡體中文 + 一般數字 · 简体中文 + 一般数字 |
| **Inter** | Google Fonts | UI, forms, labels, part numbers, data · UI/料號/標籤/數據 · UI/料号/标签/数据 |

### ⚠️ Critical Rule · 關鍵規則 · 关键规则

**[繁中]** Antonio 用於「**標題、品牌強調、醒目展示數字**」場景。一般卡片標題、按鈕、料號、Stat 大數字使用 Noto Sans / Inter。**例外**:Hero Meta 區的關鍵展示數字(如 1987、22、14、900+)使用 Antonio 36px 強化品牌儀式感。

**[English]** Antonio is for **"headings, brand emphasis, and emphatic display numerals"**. Regular card titles, buttons, part numbers, and statistical numbers use Noto Sans / Inter. **Exception**: Hero Meta key display numerals (e.g., 1987, 22, 14, 900+) use Antonio 36px to reinforce brand ritual.

**[简中]** Antonio 用于「**标题、品牌强调、醒目展示数字**」场景。一般卡片标题、按钮、料号、Stat 大数字使用 Noto Sans / Inter。**例外**:Hero Meta 区的关键展示数字(如 1987、22、14、900+)使用 Antonio 36px 强化品牌仪式感。

### Type Scale · 字級表

| Level | Font | Size | Weight | Line | Letter | Antonio? |
|---|---|---|---|---|---|---|
| Display LG | **Antonio** | 88px | 500 | 0.95 | -0.025em | ✅ |
| Section Title | **Antonio** | 72px | 500 | 1.0 | -0.02em | ✅ |
| Hero Title | **Antonio** | 88px | 400 | 0.95 | -0.025em | ✅ |
| Hero Meta Numerals (emphatic) | **Antonio** | 36px | 500 | 1.0 | -0.02em | ✅ |
| WINGO Origin Letter | **Antonio** | 56px | 500 | 1.0 | -0.025em | ✅ |
| Slogan (brand) | **Antonio** | 28px | 500 | 1.2 | 0.02em | ✅ |
| Logo (W mark) | **Antonio** | 16px | 700 | 1.0 | -0.02em | ✅ |
| Subtitle | Noto Sans | 28px | 300 | 1.3 | 0.02em | ❌ |
| H2 / Block Title | Noto Sans | 24px | 600 | 1.4 | 0.01em | ❌ |
| Card Title | Noto Sans | 22px | 600 | 1.4 | 0.01em | ❌ |
| Stat Value (numerals) | Noto Sans | 48px | 600 | 1.0 | -0.02em | ❌ |
| Slogan body | Noto Sans | 20px | 400 | 1.65 | 0.01em | ❌ |
| Body | Inter + Noto | 14px | 300 | 1.7 | - | ❌ |
| Data / Label | Inter | 11–13px | 500–700 | 1.2 | 0.08–0.1em (uppercase) | ❌ |

**Note · 注意 · 注意**:
- Do NOT use JetBrains Mono. Inter 600 with letter-spacing 0.08em achieves the same hierarchical clarity.
- 不使用 JetBrains Mono。Inter 600 配 letter-spacing 0.08em 達到相同的層級辨識度。
- 不使用 JetBrains Mono。Inter 600 配 letter-spacing 0.08em 达到相同的层级辨识度。

### Google Fonts Import

```html
<link href="https://fonts.googleapis.com/css2?family=Antonio:wght@300;400;500;600;700&family=Noto+Sans+TC:wght@300;400;500;600;700&family=Noto+Sans+SC:wght@300;400;500;600;700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

---

## 📏 03 · Spacing · 間距

**Base 4px rhythm · 4px 為基底節奏**

| Token | Value | Usage |
|---|---|---|
| `--sp-1` | 4px | Inline gap, icon padding |
| `--sp-2` | 8px | Tag padding, small gap |
| `--sp-3` | 12px | Card inner gap |
| `--sp-4` | 16px | Card padding |
| `--sp-5` | 24px | Section element gap |
| `--sp-6` | 32px | Large card padding |
| `--sp-7` | 48px | Section vertical |
| `--sp-8` | 64px | Major section |
| `--sp-9` | 88px | Hero / page padding |

**Indicator color rule · 標示軸線配色 · 标示轴线配色**:
When visualizing the spacing scale (bars, rulers, guides), use **mid gray (`--text-2` #737373) as the default**, reserving gold only for a single accent (e.g., the largest value). This keeps the "80% black-gray / 20% gold" ratio. Do not make all spacing indicators gold.
標示間距尺度時,軸線**預設用中灰 (--text-2 #737373)**,金色僅作單一強調(如最大值)。維持「黑灰 80% / 金 20%」比例,勿全部使用金色。

---

## ⭕ 04 · Radius · 圓角

| Token | Value | Usage |
|---|---|---|
| `--r-sm` | 4px | Tag, badge |
| `--r-md` | 8px | Input, small button |
| `--r-lg` | 16px | Small card |
| `--r-xl` | 28px | Mid card |
| `--r-2xl` | 32px | Large card, hero block |
| `--r-pill` | 9999px | Button, pill |

---

## 🎨 05 · (Bipolar Accent moved to Section 01)

> The Bipolar Accent pattern has been integrated into **Section 01 · Color Tokens** as "Bipolar Accent v2" since v3.9.6, since it now relies on Taiwan Semantic Colors. See Section 01 for the updated definition.

---

## 🧩 06 · Components · 元件

### Button

```css
.btn {
  font-family: 'Inter', sans-serif;
  font-size: 13px;
  font-weight: 500;
  padding: 12px 24px;
  border-radius: 9999px;
  letter-spacing: 0.03em;
}
.btn-primary { background: #1A1A1A; color: #FFFFFF; }
.btn-gold { background: #DF9C41; color: #FFFFFF; }  /* updated from #C9941F → uses Data Gold */
.btn-secondary { background: transparent; color: #1A1A1A; border: 1px solid #D4D4D4; }
.btn-ghost { background: transparent; color: #737373; padding: 12px; }
```

**Note**: Gold button uses **white text** (not black). Gold uses Data Palette's `#DF9C41` since v3.9.6.

### Card

```css
.card {
  background: #FFFFFF;                       /* white card on light-gray page */
  border: 1px solid #ECECEA;                 /* --card-border, soft */
  border-radius: 32px;
  padding: 24px;
  box-shadow: 0 1px 2px rgba(28,25,20,0.03), 0 10px 30px rgba(28,25,20,0.06);  /* warm soft shadow */
}
```

> Page background is `--page-bg` #F4F4F3 (v3.10). Cards are white and float on soft warm shadows — see "Elevation & Surface System" in Section 01.

### Stat / Data Card

- Large numeric: **Noto Sans** 600, 48px, letter-spacing -0.02em (Antonio reserved for headings only — but Hero meta數字使用 Antonio 36px 醒目展示)
- Label above: Inter 600, 11px, uppercase, letter-spacing 0.1em, color #737373
- Delta below: pill-style, **uses Taiwan Semantic Colors**:
  - `.up` → `--tw-red` #C9302C bg + white text (上漲/成長)
  - `.down` → `--tw-green` #5D8722 bg + white text (下跌/衰退)
  - `.warn` → `--tw-yellow` #DF9C41 bg + white text (注意/警示)

### Tag

```css
.tag {
  font-family: 'Inter', sans-serif;
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  padding: 4px 12px;
  border-radius: 4px;
}
```

---

## 🎨 07 · Logo · 集團 Logo · 集团 Logo

WIN-HOUSE Group provides two logo variants. Choose by context while maintaining brand consistency.

### Variant 01 · Full Wordmark · 完整商標(Logo + 文字)

**URL**: `https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/Win-House-Group-bk.png?v=1`

**Recommended Use · 建議場景 · 建议场景**:
- Website homepage, product catalog cover · 官網首頁、產品型錄封面 · 官网首页、产品型录封面
- Business card, letterhead, presentation cover · 名片、信頭紙、簡報封面 · 名片、信头纸、演示封面
- Client proposals, contracts, invoices · 客戶提案、合約、發票 · 客户提案、合约、发票

### Variant 02 · Standalone Mark · 純識別標誌(Logo Only)

**URL**: `https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/winhouse%20logo%20red.png?v=1`

**Recommended Use · 建議場景 · 建议场景**:
- Website favicon, app icon · 網站 Favicon、App icon
- Avatar, social media profile · 大頭貼、社群媒體頭像
- Product packaging, badge, stamp · 產品包裝、徽章、印章

### Logo Source Files · 原始檔

| File | Path |
|---|---|
| Adobe Illustrator (vector) | `Win-House Group-bk.ai` (in repo root) |
| Full Wordmark PNG | `Win-House-Group-bk.png` (in repo root) |
| Mark PNG | `winhouse logo red.png` (in repo root) |

### ✅ Logo Do · Logo 使用規範

- Maintain clear space of at least **1/2 logo height** around the logo
- 保留 Logo 周圍至少等同於 Logo 高度的 1/2 留白
- 保留 Logo 周围至少等同于 Logo 高度的 1/2 留白
- Prefer light backgrounds; use white mono version on dark backgrounds
- 淺色背景優先使用,深色背景需轉為單色白色版本
- 浅色背景优先使用,深色背景需转为单色白色版本
- Minimum size: Mark 24px, Wordmark 32px height
- 最小使用尺寸:Mark 24px、Wordmark 高度 32px

### ❌ Logo Don't · Logo 禁止

- Do not stretch, rotate, or recolor the logo · 不變形、不旋轉、不重新著色
- Do not overlay on busy images or low-contrast backgrounds · 不疊加在複雜圖像、低對比背景上
- Do not add shadows, strokes, gradients, or effects · 不加陰影、外框、漸層、特效

### ⚖️ Formal Document Standard · 正式文件規範 · 正式文件规范

**[繁中]** 用於**合約、報價單、發票、法律文件、正式公文**等正式場合時,除 Logo 外,必須使用**完整公司抬頭(法定登記全名)**,而非簡稱或品牌名,才符合正規與法律效力。日常行銷、簡報、網站等非正式場景可使用品牌簡稱「WIN-HOUSE Group / 文浩集團」。

**[English]** For **contracts, quotations, invoices, legal documents, and official correspondence**, the **full registered company name (legal entity title)** must be used alongside the logo — not the abbreviation or brand name — to ensure formality and legal validity. The brand short name "WIN-HOUSE Group" may be used for marketing, presentations, websites, and other informal contexts.

**[简中]** 用于**合约、报价单、发票、法律文件、正式公文**等正式场合时,除 Logo 外,必须使用**完整公司抬头(法定登记全名)**,而非简称或品牌名,才符合正规与法律效力。日常营销、演示、网站等非正式场景可使用品牌简称「WIN-HOUSE Group / 文浩集团」。

| Context · 場景 | Name to Use · 使用名稱 |
|---|---|
| Contracts, invoices, legal docs · 合約、發票、法律文件 | Full registered company name · 完整公司抬頭(法定全名) |
| Marketing, web, presentations · 行銷、網站、簡報 | Brand short name · 品牌簡稱(WIN-HOUSE Group / 文浩集團) |

---

## 🦅 08 · WINGO Mascot · 吉祥物

### Identity · 形象 · 形象

**[繁中]** WINGO 是 WIN-HOUSE 文浩集團的 AI 導航員。他擅長在複雜資訊中,找出真正有價值的機會,每一次挑戰,都是成長的開始。**YOUR BEST PARTNER!**

**[English]** WINGO is the AI Navigator of WIN-HOUSE Group. He excels at finding genuinely valuable opportunities within complex information — every challenge marks the beginning of growth. **YOUR BEST PARTNER!**

**[简中]** WINGO 是 WIN-HOUSE 文浩集团的 AI 导航员。他擅长在复杂信息中,找出真正有价值的机会,每一次挑战,都是成长的开始。**YOUR BEST PARTNER!**

### Visual Spec · 視覺規格 · 视觉规格

- **Species · 物種**: Eagle / 老鷹 / 老鹰
- **Outfit · 著裝**: Black business suit, red tie, WH red logo on chest, yellow beak and feet
- **Palette · 配色**: Black · White · Red · Gold
- **Role · 定位**: AI Sales Navigator / AI 業務導航員 / AI 业务导航员
- **Tone · 語氣**: Warm · Professional / 親切 · 專業 / 亲切 · 专业

### The Story Behind the Name · WINGO 命名背景

The name WINGO derives from three layered meanings · WINGO 這個名字結合三層意義 · WINGO 名字结合三层含义:

| Letter | Meaning · 繁中 · 简中 · English |
|---|---|
| **WIN** | 勝利 · 成交 · 前進 / 胜利 · 成交 · 前进 / Victory · Closing · Forward |
| **WING** | 翅膀 · 視野 · 導航 / 翅膀 · 视野 · 导航 / Wings · Vision · Navigation |
| **GO** | 行動 · 挑戰 · 成長 / 行动 · 挑战 · 成长 / Action · Challenge · Growth |

**[繁中]** 結合文浩的企業核心,WINGO 代表的是 — 陪伴文浩團隊一起判斷、行動、成交的 AI 業務導航員。

**[English]** Combined with WIN-HOUSE's core spirit, WINGO embodies — the AI Sales Navigator who walks alongside the WIN-HOUSE team to judge, act, and close deals together.

**[简中]** 结合文浩的企业核心,WINGO 代表的是 — 陪伴文浩团队一起判断、行动、成交的 AI 业务导航员。

### Usage Rule · 使用規則 · 使用规则

✅ **DO use in** · 適用場景 · 适用场景:
- Internal tool UI, LINE weekly report covers, training materials
- 內部工具 UI、LINE 週報封面、訓練教材
- 内部工具 UI、LINE 周报封面、训练教材
- Employee activities, presentation interior pages, sales LINE cards
- 員工活動、簡報內頁、業務 LINE 圖卡
- 员工活动、演示内页、业务 LINE 图卡
- System notification pages, soft website pages, LinkedIn soft posts
- 系統提示頁、官網軟性頁、LinkedIn 軟性貼文
- 系统提示页、官网软性页、LinkedIn 软性贴文

❌ **DO NOT use in** · 不適用場景 · 不适用场景:
- Official website homepage, product catalogs, datasheets
- 官網首頁、產品型錄、Datasheet
- 官网首页、产品型录、Datasheet
- Quotes, contracts, manufacturer co-branded materials
- 報價單、合約、原廠共同露出素材
- 报价单、合约、原厂共同露出素材
- Client proposals, presentation covers/back covers, large red backgrounds
- 客戶提案、簡報封面/封底、大紅底背景
- 客户提案、演示封面/封底、大红底背景

### Decision Rules · 判斷原則 · 判断原则

| Use WINGO · 用 | Skip WINGO · 不用 |
|---|---|
| Warmth → Use · 親切 → 上場 · 亲切 → 上场 | Premium → Hold back · 專業 → 收斂 · 专业 → 收敛 |
| For employees → Fit · 員工看的 → 適合 · 员工看的 → 适合 | For clients & formal business → Skip · 客戶 & 硬性業務 → 不用 · 客户 & 硬性业务 → 不用 |

### Assets · 資產

| Asset | URL |
|---|---|
| WINGO Hi (greeting) | `https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/wingo/wingo-hi.png?v=2` |

**Current assets**: 1 · Greeting (Hi). New poses, expressions, and UI components will be added to the `wingo/` folder. URL pattern: `cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/wingo/[filename].png?v=N` — increment `?v=N` when the same filename is replaced to force CDN cache refresh.

---

## 🚫 09 · Strict Prohibitions · 禁止事項

These violate the design system. NEVER use:

| ❌ Prohibited | ✅ Use Instead |
|---|---|
| Saturated gold #EAB308 (Havn original) | `--data-gold` #DF9C41 |
| Old `--gold` #C9941F (brand color deprecated v3.9.6) | `--data-gold` #DF9C41 (from Data Palette) |
| Old `--slate-blue` #4A6B8A (brand color deprecated v3.9.6) | `--data-blue-deep` #2677A5 (from Data Palette) |
| Old `--clay` #B57258 (brand color deprecated v3.9.6) | `--data-rust` #923621 (from Data Palette) |
| Old `--sage` #5A8159 (brand color deprecated v3.9.6) | `--data-green` #5D8722 (from Data Palette) |
| Pure red #FF0000 or warning red | `--tw-red` #C9302C or `--tw-yellow` #DF9C41 |
| Purple gradients, blue-purple tech aesthetic | `--data-blue-deep` #2677A5 solid |
| Bright/fluorescent yellow | `--tw-yellow` #DF9C41 (muted warm) |
| Serif Chinese fonts (宋體) | Noto Sans TC/SC sans-serif |
| Logo Red #E1251B as background fill | Logo only |
| JetBrains Mono / Fira Code | Inter 600 + uppercase letter-spacing |
| **Green-up / Red-down (Western convention)** | **Red=up / Green=down / Yellow=warn (Greater-China convention)** |
| Black text on Gold button | White text on Gold button |
| "Bald Eagle / 白頭海鵰" species | Just "Eagle / 老鷹" |
| WINGO in formal external materials | WINGO internal only |
| Antonio for regular card titles, buttons, part numbers | Noto Sans / Inter |
| Gold over 10% of viewport area | Keep Gold 5–10% for accent only |
| Data palette as primary brand identity | Data palette for charts + accent usage |
| **Full-black background for tables/data blocks** | **Light surfaces (`--surface-1`); reserve black for Hero only** |
| **Blue text on white background** | **Black/gray text; blue only as fill/border or on dark surfaces** |
| **Bright gold #DF9C41 as small text on white** | **Deep gold `--gold-hover` #AF7231 for small text (better contrast)** |

---

## 📁 10 · CDN-Referenced Resources · CDN 引用資源

All Win-House design resources are hosted on GitHub + jsDelivr CDN + GitHub Pages, accessible from any AI or external system:

| Resource | URL |
|---|---|
| **This spec (Markdown)** | `https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/design-system/SPEC.md` |
| **Interactive HTML spec** | `https://timfan119.github.io/winhouse-brand-assets/design-system/` |
| WINGO Hi greeting | `https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/wingo/wingo-hi.png?v=2` |
| Group Logo (full wordmark) | `https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/Win-House-Group-bk.png?v=1` |
| Group Logo (standalone mark) | `https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/winhouse%20logo%20red.png?v=1` |
| Logo source AI file | `https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/Win-House%20Group-bk.ai` |
| WINGO image fallback (raw) | `https://raw.githubusercontent.com/timfan119/winhouse-brand-assets/main/wingo/wingo-hi.png` |
| Brand README | `https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/README.md` |
| GitHub Repo | `https://github.com/timfan119/winhouse-brand-assets` |

### 🔄 Cache-Busting Strategy · 快取破解策略 · 缓存破解策略

**[繁中]** jsDelivr CDN 預設快取檔案 7 天。當 GitHub 上覆蓋同名檔案時,CDN 仍會回傳舊版。所有圖片資源 URL 一律加上 `?v=N` query 參數作為版本流水號:
- 首次發布:`wingo-hi.png?v=1`(或無參數)
- 替換同名檔案後,把 `?v=N` 改為 `?v=N+1`(例如 v=2、v=3...)
- 緊急情況可訪問 `https://purge.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/wingo/wingo-hi.png` 手動清快取

**[English]** jsDelivr CDN caches files for 7 days by default. When a same-name file is replaced on GitHub, the CDN still serves the old version. All image asset URLs MUST include a `?v=N` query parameter as a version counter:
- First release: `wingo-hi.png?v=1` (or no parameter)
- After replacing the same filename: increment `?v=N` to `?v=N+1` (e.g., v=2, v=3...)
- For immediate purge: visit `https://purge.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/wingo/wingo-hi.png`

**[简中]** jsDelivr CDN 默认缓存文件 7 天。当 GitHub 上覆盖同名文件时,CDN 仍会返回旧版。所有图片资源 URL 一律加上 `?v=N` query 参数作为版本流水号:
- 首次发布:`wingo-hi.png?v=1`(或无参数)
- 替换同名文件后,把 `?v=N` 改为 `?v=N+1`(例如 v=2、v=3...)
- 紧急情况可访问 `https://purge.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/wingo/wingo-hi.png` 手动清缓存

**Current cache version**: `?v=2` (updated 2026-05-26 to fix outdated WINGO image cached from v=1)

---

## 🤖 11 · AI Prompt Template · 給 AI 的指令範本

**For ChatGPT / Claude / Gemini / any AI** — copy and paste this when requesting Win-House design output:

> I am working with WIN-HOUSE Group (文浩集團), a Taiwan-based passive electronic components distributor founded in 1987.
>
> Before producing any visual or frontend output, you MUST follow our Design System v3.10.0. Fetch the full spec from:
> https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/design-system/SPEC.md
>
> Or view the interactive spec page:
> https://timfan119.github.io/winhouse-brand-assets/design-system/
>
> Key constraints (non-negotiable):
> - **Only ONE protected brand color**: Logo Red #E1251B (LOGO ONLY, never as background)
> - **Black/white/gray dominant** (80%+ of viewport)
> - **Data Palette** (9 colors, replaces old brand 5-color): #E4AF79, #DF9C41, #AF7231, #923621, #2D2A28, #2677A5, #639BC1, #90A74A, #5D8722
> - **Semantic Colors** (Greater-China convention):
>   - Red #C9302C = UP / growth
>   - Green #5D8722 = DOWN / decline
>   - Yellow #DF9C41 = WARN / attention
> - **Application Domain Mapping** (for industry charts):
>   - Optical 光通訊 → #E4AF79 (warm light)
>   - Automotive 汽車 → #2677A5 (deep blue)
>   - Networking 網通 → #639BC1 (light blue)
>   - Industrial 工業 → #AF7231 (bronze)
>   - Power 電源 → #923621 (rust)
>   - Consumer 消費電子 → #DF9C41 (warm gold)
>   - Robotics 機器人 → #2D2A28 (charcoal)
>   - Drone 無人機 → #90A74A (olive)
>   - AR / Satellite → #5D8722 (deep green)
> - **Fonts**: Antonio for headings/Hero/Logo/**emphatic display numerals** (e.g., Hero meta stats); Noto Sans TC/SC for Chinese + regular card titles + stat values; Inter for UI/data labels
> - **Pill buttons** (radius 9999px), card radius 32px, base 4px spacing
> - **WINGO mascot** (eagle, NOT bald eagle) only for internal/warm scenarios — never for formal external output
> - WINGO image: https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/wingo/wingo-hi.png?v=2
> - **Group Logo** (two variants):
>   - Full wordmark (logo + text): https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/Win-House-Group-bk.png?v=1
>   - Standalone mark: https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/winhouse%20logo%20red.png?v=1
> - **Formal documents** (contracts, invoices, legal docs): use the FULL registered company name, not the brand short name. Brand short name "WIN-HOUSE Group" is for informal/marketing use only.
>
> Now produce: [your request here]
>
> Now produce: [your request here]
>
> Now produce: [your request here]

---

## 📝 12 · Version History · 版本紀錄

| Version | Date | Note |
|---|---|---|
| **v3.10.0** | 2026-06-11 | **Production** · Muze-inspired elevation system (color unchanged): light-gray page bg `--page-bg` #F4F4F3, top-level containers inverted to white cards with soft warm shadows, `--card-border` #ECECEA, sticky topnav float, Hero elevated. |
| v3.9.14 | 2026-05-26 | Removed duplicate "YOUR BEST PARTNER!" slogan from WINGO name-origin block (kept once in WINGO intro). |
| v3.9.13 | 2026-05-26 | Formal Document Standard added — full registered company name required for contracts/invoices/legal docs; brand short name for informal contexts. |
| v3.9.12 | 2026-05-26 | Spacing indicator bars use mid gray `--text-2` #737373 (auxiliary level), not near-black. |
| v3.9.11 | 2026-05-26 | Spacing indicator bars default to gray, gold reserved as single accent (80/20 ratio). |
| v3.9.10 | 2026-05-26 | Text & background rules added — no full-black table backgrounds (AI-ref block lightened to light surface), no blue text on white, deep gold `--gold-hover` for small text legibility. |
| v3.9.9 | 2026-05-26 | Topnav logo upgraded to full wordmark PNG. Data Palette swatches regrouped by adjacency (Warm / Cool / Neutral). Dashboard color usage refined into 3 strategies (Gradient / Dual Axis / Contrast). |
| v3.9.8 | 2026-05-26 | Logo section added (full wordmark + standalone mark on GitHub root). WINGO usage rules visually updated to green-check / red-cross. |
| v3.9.7 | 2026-05-26 | Application Domain Color Mapping introduced (9 industries) |
| v3.9.6 | 2026-05-26 | Brand 5-color deprecated, Semantic Colors introduced |
| v3.9.5 | 2026-05-26 | Gold usage reduced 10%, font rule clarified, Data Palette added |
| v3.9.4 | 2026-05-26 | CDN cache-busting via `?v=N` query param on image URLs |
| v3.9.3 | 2026-05-26 | WINGO header restructure (image beside title), slogan typography 20px/28px upgrade |
| v3.9.2 | 2026-05-26 | Species fix (Eagle, not Bald Eagle), robust image fallback chain |
| v3.9.1 | 2026-05-26 | WINGO image fallback added, title hierarchy refinement |
| v3.9 | 2026-05-26 | WINGO storytelling: WIN+WING+GO origin background, decision rules |
| v3.8 | 2026-05-26 | Tri-lingual support (繁中 / 简中 / EN) with localStorage persistence |
| v3.7 | 2026-05-25 | Mandatory unified standard · CDN-hosted spec |
| v3.6 | 2026-05-25 | WINGO integrated via CDN |
| v3.0–v3.5 | 2026-05-25 | Iterative refinement (deprecated) |
| v2 | 2025-12 | B&W + mustard yellow exploration (deprecated) |

---

© WIN-HOUSE Group · 文浩集團 · Since 1987
"Your Best Partner!" · 樂觀進取
