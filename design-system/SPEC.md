# WIN-HOUSE Design System v3.9.4 · Official Specification

**版本** Version: v3.9.4 (Production)
**狀態** Status: Active · Mandatory
**最後更新** Last Updated: 2026-05-26
**規範負責人** Owner: Tim Fan, CEO, WIN-HOUSE Group

---

## ⚠️ 強制聲明 · MANDATORY NOTICE · 强制声明

**[繁中]** 本規範為文浩集團統一視覺準則,適用於所有 frontend 介面、內部工具、對外網站、簡報範本、AI 生成素材與跨語系頁面。任何 AI、設計師、外包合作夥伴產出 Win-House 視覺素材前,**必須先讀取本規範**並嚴格遵循。本文件取代過往所有版本(v2、v3.0–v3.9.3 全部廢止)。

**[English]** This specification is the unified visual standard for WIN-HOUSE Group, applicable to all frontend interfaces, internal tools, external websites, presentation templates, AI-generated assets, and multi-language pages. Any AI, designer, or third-party partner producing visual materials for WIN-HOUSE **must read this specification first** and follow it strictly. This document supersedes all previous versions (v2, v3.0–v3.9.3 are deprecated).

**[简中]** 本规范为文浩集团统一视觉准则,适用于所有 frontend 界面、内部工具、对外网站、演示模板、AI 生成素材与跨语种页面。任何 AI、设计师、外包合作伙伴产出 Win-House 视觉素材前,**必须先读取本规范**并严格遵循。本文件取代过往所有版本(v2、v3.0–v3.9.3 全部废止)。

---

## 📐 01 · Color Tokens · 配色 · 配色

### Brand Anchors · 五大品牌色

| Token | HEX | Role · 用途 · 用途 |
|---|---|---|
| `--gold` | `#C9941F` | Primary brand color · 主色強調 / 正向 / Do · 主色强调 / 正向 / Do |
| `--logo-red` | `#E1251B` | Logo only, never as background · 僅 Logo 使用 · 仅 Logo 使用 |
| `--slate-blue` | `#4A6B8A` | Accent / Info / Negative / Don't · 調和色 / 資訊 / 負向 · 调和色 / 信息 / 负向 |
| `--clay` | `#B57258` | Warning / error · 警示 / 錯誤 · 警示 / 错误 |
| `--sage` | `#5A8159` | Success state · 成功狀態 · 成功状态 |

### Surfaces · 表面色

| Token | HEX | Role |
|---|---|---|
| `--bg` | `#FFFFFF` | Page background · 頁面背景 |
| `--surface-1` | `#F5F5F5` | Card background · 卡片底 |
| `--surface-2` | `#FAFAFA` | Secondary surface · 次層表面 |
| `--text-1` | `#1A1A1A` | Primary text · 主文字 |
| `--text-2` | `#737373` | Secondary text · 次文字 |
| `--text-3` | `#A3A3A3` | Tertiary text · 輔助文字 |
| `--border` | `#E5E5E5` | Border · 邊框 |
| `--hero-bg` | `#0A0A0A` | Hero showcase only · Hero 展示專用 |

---

## ✍️ 02 · Typography · 字體 · 字体

**四套字體分工 · Four-Font System · 四套字体分工**

| Font Family | Source | Usage · 用途 · 用途 |
|---|---|---|
| **Antonio** | Google Fonts | English headings, display, numerals · 英文標題/數字/Display · 英文标题/数字/Display |
| **Noto Sans TC** | Google Fonts | Traditional Chinese · 繁體中文 · 繁体中文 |
| **Noto Sans SC** | Google Fonts | Simplified Chinese · 簡體中文 · 简体中文 |
| **Inter** | Google Fonts | UI, forms, labels, part numbers, data · UI/料號/標籤/數據 · UI/料号/标签/数据 |

### Type Scale · 字級表

| Level | Font | Size | Weight | Line | Letter |
|---|---|---|---|---|---|
| Display LG | Antonio | 88px | 500 | 0.95 | -0.025em |
| Section Title | Antonio | 72px | 500 | 1.0 | -0.02em |
| H1 | Antonio | 56px | 500 | 1.0 | -0.02em |
| Subtitle | Noto Sans | 28px | 300 | 1.3 | 0.02em |
| H2 / Block Title | Noto Sans | 24px | 600 | 1.4 | 0.01em |
| Slogan | Noto Sans | 20px | 400 | 1.65 | 0.01em |
| Body | Inter + Noto | 14px | 300 | 1.7 | - |
| Data / Label | Inter | 11–13px | 500–700 | 1.2 | 0.08–0.1em (uppercase) |

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

## 🎨 05 · Bipolar Accent · 雙極對比制 · 双极对比制

**Win-House signature pattern**:
Gold (正向 / Do / Up) vs Slate Blue (負向 / Don't / Down)

| Context | Positive · 正向 · 正向 | Negative · 負向 · 负向 |
|---|---|---|
| Stat Delta | Gold #C9941F bg + white text | Slate Blue #4A6B8A bg + white text |
| Do / Don't | Gold border-left 4px + gold soft bg | Slate Blue border-left 4px + slate soft bg |
| WINGO Decision | Gold "warmth / 親切 / use" | Slate Blue "premium / 專業 / hold" |

**Why · 為什麼 · 为什么**:
- Avoids the generic green/red SaaS aesthetic.
- 避免泛用的綠紅 SaaS 視覺。
- 避免泛用的绿红 SaaS 视觉。
- Gold = brand achievement; Slate Blue = calm review (not alarm).
- 金色 = 品牌成就感;石板藍 = 冷靜檢討(非警報)。
- 金色 = 品牌成就感;石板蓝 = 冷静检讨(非警报)。

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
.btn-gold { background: #C9941F; color: #FFFFFF; }  /* white text, NOT black */
.btn-secondary { background: transparent; color: #1A1A1A; border: 1px solid #D4D4D4; }
.btn-ghost { background: transparent; color: #737373; padding: 12px; }
```

**Note**: Gold button uses **white text** (not black). 金色按鈕用白字非黑字。

### Card

```css
.card {
  background: #FFFFFF;
  border: 1px solid #E5E5E5;
  border-radius: 32px;
  padding: 24px;
  box-shadow: 0 1px 2px rgba(0,0,0,0.04), 0 8px 24px rgba(0,0,0,0.04);
}
```

### Stat / Data Card

- Large numeric: Antonio 500, 56px, letter-spacing -0.025em
- Label above: Inter 600, 11px, uppercase, letter-spacing 0.1em, color #737373
- Delta below: pill-style, Gold (up) or Slate Blue (down), white text

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

## 🦅 07 · WINGO Mascot · 吉祥物

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

## 🚫 08 · Strict Prohibitions · 禁止事項

These violate the design system. NEVER use:

| ❌ Prohibited | ✅ Use Instead |
|---|---|
| Saturated gold #EAB308 (Havn original) | #C9941F (Win-House gold) |
| Pure red #FF0000 or warning red | #B57258 Clay |
| Purple gradients, blue-purple tech aesthetic | Slate Blue #4A6B8A solid |
| Bright/fluorescent yellow | Muted gold #C9941F |
| Serif Chinese fonts (宋體) | Noto Sans TC/SC sans-serif |
| Logo Red as background fill | Gold or Hero black bg |
| JetBrains Mono / Fira Code | Inter 600 + uppercase letter-spacing |
| Generic green/red for up/down | Bipolar Accent (Gold/Slate Blue) |
| Black text on Gold button | White text on Gold button |
| "Bald Eagle / 白頭海鵰" species | Just "Eagle / 老鷹" |
| WINGO in formal external materials | WINGO internal only |

---

## 📁 09 · CDN-Referenced Resources · CDN 引用資源

All Win-House design resources are hosted on GitHub + jsDelivr CDN + GitHub Pages, accessible from any AI or external system:

| Resource | URL |
|---|---|
| **This spec (Markdown)** | `https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/design-system/SPEC.md` |
| **Interactive HTML spec** | `https://timfan119.github.io/winhouse-brand-assets/design-system/` |
| WINGO Hi greeting | `https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/wingo/wingo-hi.png?v=2` |
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

## 🤖 10 · AI Prompt Template · 給 AI 的指令範本

**For ChatGPT / Claude / Gemini / any AI** — copy and paste this when requesting Win-House design output:

> I am working with WIN-HOUSE Group (文浩集團), a Taiwan-based passive electronic components distributor founded in 1987.
>
> Before producing any visual or frontend output, you MUST follow our Design System v3.9.4. Fetch the full spec from:
> https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/design-system/SPEC.md
>
> Or view the interactive spec page:
> https://timfan119.github.io/winhouse-brand-assets/design-system/
>
> Key constraints (non-negotiable):
> - Primary color: Gold #C9941F (not yellow, not orange)
> - Bipolar accent: Gold (positive) vs Slate Blue #4A6B8A (negative); never use green/red
> - Fonts: Antonio (English headings/numerals), Noto Sans TC/SC (Chinese), Inter (UI/data)
> - Logo Red #E1251B is for logo ONLY, never as background
> - Pill-shape buttons (radius 9999px), card radius 32px, base 4px spacing
> - WINGO mascot (eagle, NOT bald eagle) only for internal/warm scenarios — never for formal external output
> - WINGO image: https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/wingo/wingo-hi.png?v=2
>
> Now produce: [your request here]

---

## 📝 11 · Version History · 版本紀錄

| Version | Date | Note |
|---|---|---|
| **v3.9.4** | 2026-05-26 | **Production** · CDN cache-busting via `?v=N` query param on image URLs to force refresh after file replacement |
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
