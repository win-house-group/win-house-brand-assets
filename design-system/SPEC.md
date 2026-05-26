# WIN-HOUSE Design System v3.7 · Official Specification

**版本** Version: v3.7 (Production)
**狀態** Status: Active · Mandatory
**最後更新** Last Updated: 2026-05-26
**規範負責人** Owner: Tim Fan, CEO, WIN-HOUSE Group

---

## ⚠️ 強制聲明 · MANDATORY NOTICE · 强制声明

**[繁中]** 本規範為文浩集團統一視覺準則,適用於所有 frontend 介面、內部工具、對外網站、簡報範本、AI 生成素材與跨語系頁面。任何 AI、設計師、外包合作夥伴產出 Win-House 視覺素材前,**必須先讀取本規範**並嚴格遵循。本文件取代過往所有版本(v2、v3.0–v3.6 全部廢止)。

**[English]** This specification is the unified visual standard for WIN-HOUSE Group, applicable to all frontend interfaces, internal tools, external websites, presentation templates, AI-generated assets, and multi-language pages. Any AI, designer, or third-party partner producing visual materials for WIN-HOUSE **must read this specification first** and follow it strictly. This document supersedes all previous versions (v2, v3.0–v3.6 are deprecated).

**[简中]** 本规范为文浩集团统一视觉准则,适用于所有 frontend 界面、内部工具、对外网站、演示模板、AI 生成素材与跨语种页面。任何 AI、设计师、外包合作伙伴产出 Win-House 视觉素材前,**必须先读取本规范**并严格遵循。本文件取代过往所有版本(v2、v3.0–v3.6 全部废止)。

---

## 📐 01 · Color Tokens · 配色 · 配色

### Brand Anchors · 五大品牌色

| Token | HEX | Role · 用途 · 用途 |
|---|---|---|
| `--gold` | `#C9941F` | Primary brand color · 主色強調 · 主色强调 |
| `--logo-red` | `#E1251B` | Logo only, never as background · 僅 Logo 使用 · 仅 Logo 使用 |
| `--slate-blue` | `#4A6B8A` | Accent / info / negative · 調和色/資訊/負向 · 调和色/信息/负向 |
| `--clay` | `#B57258` | Warning / error · 警示/錯誤 · 警示/错误 |
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

**三套字體分工 · Three-Font System · 三套字体分工**

| Font Family | Source | Usage · 用途 · 用途 |
|---|---|---|
| **Antonio** | Google Fonts | English headings, display, numerals · 英文標題/數字/Display · 英文标题/数字/Display |
| **Noto Sans TC** | Google Fonts | All Traditional Chinese · 所有繁體中文 · 所有繁体中文 |
| **Inter** | Google Fonts | UI, forms, labels, part numbers, data · UI/料號/標籤/數據 · UI/料号/标签/数据 |

### Type Scale · 字級表

| Level | Font | Size | Weight | Line | Letter |
|---|---|---|---|---|---|
| Display LG | Antonio | 88px | 500 | 0.95 | -0.025em |
| H1 | Antonio | 56px | 500 | 1.0 | -0.02em |
| H1 CN | Noto Sans TC | 36px | 500 | 1.3 | 0.01em |
| H2 CN | Noto Sans TC | 24px | 400 | 1.4 | - |
| Body | Inter + Noto | 14px | 300 | 1.7 | - |
| Data / Label | Inter | 11–13px | 500–700 | 1.2 | 0.08–0.1em (uppercase) |

**Note · 注意 · 注意**:
- Do NOT use JetBrains Mono. Inter 600 with letter-spacing 0.08em achieves the same hierarchical clarity.
- 不使用 JetBrains Mono。Inter 600 配 letter-spacing 0.08em 達到相同的層級辨識度。
- 不使用 JetBrains Mono。Inter 600 配 letter-spacing 0.08em 达到相同的层级辨识度。

### Google Fonts Import

```html
<link href="https://fonts.googleapis.com/css2?family=Antonio:wght@300;400;500;600;700&family=Noto+Sans+TC:wght@300;400;500;600;700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
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
Gold (正向/Do/Up) vs Slate Blue (負向/Don't/Down)

| Context | Positive · 正向 · 正向 | Negative · 負向 · 负向 |
|---|---|---|
| Stat Delta | Gold #C9941F bg + white text | Slate Blue #4A6B8A bg + white text |
| Do / Don't | Gold border-left 4px + gold soft bg | Slate Blue border-left 4px + slate soft bg |
| Toggle State | Gold filled | Slate Blue filled |

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
- Delta below: pill-style, Gold(up) or Slate Blue(down), white text

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

## 🐦 07 · WINGO Mascot · 吉祥物

**Permanent CDN URL pattern**:
```
https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/wingo/[filename].png
```

**Identity · 形象**:
Bald eagle in black suit, red tie, WH red logo on chest, yellow beak and feet. Slogan: "Your Best Partner".

**Usage Rule · 使用規則 · 使用规则**:

✅ **DO use in** · 適用 · 适用:
- Internal tools (career framework, KPI dashboards) · 內部工具 · 内部工具
- LINE weekly reports · LINE 週報 · LINE 周报
- Training materials · 訓練教材 · 训练教材
- Empty state, success/level-up prompts · 系統提示 · 系统提示

❌ **DO NOT use in** · 排除 · 排除:
- Official website hero · 官網首頁 · 官网首页
- Product catalogs, datasheets · 產品型錄 · 产品型录
- Quotes, contracts, invoices · 報價/契約 · 报价/契约
- Tier 1 client proposal covers · Tier 1 提案 · Tier 1 提案
- Co-branded materials with principals · 原廠共同露出 · 原厂共同露出
- Large red background scenes · 大紅底場景 · 大红底场景

**Decision rule · 判斷準則 · 判断准则**:
"Warmth vs Premium professionalism" — when the scene needs warmth, use WINGO; when it needs premium professional gravitas, exclude WINGO. Always ask the user before adding WINGO to any new asset type.

---

## 🚫 08 · Strict Prohibitions · 禁止事項

These violate the design system. NEVER use:

| ❌ Prohibited | ✅ Use Instead |
|---|---|
| Saturated gold #EAB308 (Havn original) | #C9941F (Win-House gold) |
| Pure red #FF0000 or warning red | #B57258 Clay |
| Purple gradients, blue-purple tech aesthetic | Slate Blue #4A6B8A solid |
| Bright/fluorescent yellow | Muted gold #C9941F |
| Serif Chinese fonts (宋體) | Noto Sans TC sans-serif |
| Logo Red as background fill | Gold or Hero black bg |
| JetBrains Mono / Fira Code | Inter 600 + uppercase letter-spacing |
| Generic green/red for up/down | Bipolar Accent (Gold/Slate Blue) |
| Black text on Gold button | White text on Gold button |

---

## 📁 09 · CDN-Referenced Resources · CDN 引用資源

All Win-House design resources are hosted on GitHub + jsDelivr CDN, accessible from any AI or external system:

| Resource | URL |
|---|---|
| This spec (Markdown) | `https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/design-system/SPEC.md` |
| Interactive HTML spec | `https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/design-system/index.html` |
| WINGO Hi greeting | `https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/wingo/wingo-hi.png` |
| Brand README | `https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/README.md` |

---

## 🤖 10 · AI Prompt Template · 給 AI 的指令範本

**For ChatGPT / Claude / Gemini / any AI** — copy and paste this when requesting Win-House design output:

> I am working with WIN-HOUSE Group (文浩集團), a Taiwan-based passive electronic components distributor founded in 1987.
>
> Before producing any visual or frontend output, you MUST follow our Design System v3.7. Fetch the full spec from:
> https://cdn.jsdelivr.net/gh/timfan119/winhouse-brand-assets@main/design-system/SPEC.md
>
> Key constraints (non-negotiable):
> - Primary color: Gold #C9941F (not yellow, not orange)
> - Bipolar accent: Gold (positive) vs Slate Blue #4A6B8A (negative); never use green/red
> - Fonts: Antonio (English headings/numbers), Noto Sans TC (Chinese), Inter (UI/data)
> - Logo Red #E1251B is for logo ONLY, never as background
> - Pill-shape buttons (radius 9999px), card radius 32px, base 4px spacing
> - WINGO mascot only for internal/warm scenarios, never for formal external output
>
> Now produce: [your request here]

---

## 📝 11 · Version History · 版本紀錄

| Version | Date | Note |
|---|---|---|
| v3.7 | 2026-05-26 | **Production** · Mandatory unified standard · CDN-hosted spec |
| v3.6 | 2026-05-25 | WINGO integrated via CDN |
| v3.0–v3.5 | 2026-05-25 | Iterative refinement (deprecated) |
| v2 | 2025-12 | B&W + mustard yellow exploration (deprecated) |

---

© WIN-HOUSE Group · 文浩集團 · Since 1987
"Your Best Partner!" · 樂觀進取
