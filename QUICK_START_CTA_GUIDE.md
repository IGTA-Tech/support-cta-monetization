# 🚀 Quick Start Guide: Support CTA Implementation

**For:** Developer implementing Support CTA buttons
**Priority:** Live sites first (custom domains → Netlify/Vercel → others)
**Full Details:** See `DEVELOPER_CTA_IMPLEMENTATION_BRIEF.md`

---

## ⚡ Quick Overview

Add this button to all live websites:
```
[Support & Build With Us] → https://support.innovativeautomations.dev/
```

**Position:** Fixed bottom-right corner
**Style:** Minimal pill button, auto dark/light mode
**Config:** Via `IA_SUPPORT_CTA_URL` env variable

---

## 📋 Top 8 Priority Sites (Do These First!)

### 🔴 Custom Domains (URGENT)
1. ✅ **faithandpolicy.com** - https://github.com/IGTA-Tech/biblical-political-analyzer (Private)
2. ✅ **placementsproposal.com** - https://github.com/IGTA-Tech/placement-investment-proposal (Private)

### 🟠 Live Netlify/Vercel Sites
3. 🌐 https://lido-partnership-proposal.netlify.app - https://github.com/IGTA-Tech/lido-proposal
4. 🌐 https://visa-glow-tool.netlify.app - https://github.com/IGTA-Tech/visa-glow-tool (Private)
5. 🌐 https://spaces-by-premier.netlify.app - https://github.com/IGTA-Tech/spaces-by-premier
6. 🌐 https://evaluation-tool-jacksonwink.netlify.app - https://github.com/IGTA-Tech/evaluation-tool-jacksonwink (Private)
7. 🌐 https://p2025-theta.vercel.app - https://github.com/IGTA-Tech/p2025
8. 🌐 https://multi-brand-email-automation.netlify.app - https://github.com/IGTA-Tech/multi-brand-email-automation

---

## 🛠️ 3-Step Implementation (Per Repo)

### Step 1: Add JavaScript File
Create `public/ia-support-cta.js`:
```javascript
(function () {
  try {
    if (window.IA_SUPPORT_CTA_DISABLE === true || window.IA_SUPPORT_CTA_DISABLE === 'true') return;
    var href = window.__IA_SUPPORT_CTA_URL__ || 'https://support.innovativeautomations.dev/';
    if (typeof href !== 'string' || !/^https?:\/\//.test(href)) {
      href = 'https://support.innovativeautomations.dev/';
    }
    if (!document.getElementById('ia-cta-style')) {
      var style = document.createElement('style');
      style.id = 'ia-cta-style';
      style.textContent = `:root{--ia-cta-bg:#111;--ia-cta-text:#fff;--ia-cta-radius:9999px;--ia-cta-shadow:0 6px 20px rgba(0,0,0,.15)}@media (prefers-color-scheme:dark){:root{--ia-cta-bg:#fff;--ia-cta-text:#111}}.ia-cta{position:fixed;bottom:20px;right:20px;z-index:99999;display:inline-flex;align-items:center;justify-content:center;padding:10px 14px;min-height:44px;min-width:44px;background:var(--ia-cta-bg);color:var(--ia-cta-text);border-radius:var(--ia-cta-radius);box-shadow:var(--ia-cta-shadow);font:600 14px/1.1 system-ui,-apple-system,Segoe UI,Roboto,sans-serif;text-decoration:none;transition:transform .15s ease,box-shadow .15s ease}@media (prefers-reduced-motion:reduce){.ia-cta{transition:none}}.ia-cta:focus,.ia-cta:hover{outline:none;transform:translateY(-1px);text-decoration:underline}.ia-cta:focus-visible{box-shadow:0 0 0 3px rgba(99,102,241,.35),var(--ia-cta-shadow)}`;
      document.head.appendChild(style);
    }
    if (document.querySelector('.ia-cta')) return;
    var a = document.createElement('a');
    a.className = 'ia-cta';
    a.href = href;
    a.target = '_blank';
    a.rel = 'noopener noreferrer';
    a.setAttribute('aria-label', 'Support and build with us');
    a.textContent = 'Support & Build With Us';
    var extraBottom = 0;
    var blockers = document.querySelector('[data-cookie-banner], .cookie, .cc-window, .chat-widget');
    if (blockers) extraBottom = 52;
    a.style.bottom = (20 + extraBottom) + 'px';
    document.addEventListener('DOMContentLoaded', function () {
      document.body.appendChild(a);
    });
  } catch (e) {}
})();
```

### Step 2: Wire It Up (Framework Specific)

**Next.js (App Router)** - `app/layout.tsx`:
```tsx
<body>
  {children}
  <script dangerouslySetInnerHTML={{__html: `window.__IA_SUPPORT_CTA_URL__ = '${process.env.IA_SUPPORT_CTA_URL ?? 'https://support.innovativeautomations.dev/'}';`}} />
  <script defer src="/ia-support-cta.js"></script>
</body>
```

**Next.js (Pages Router)** - `pages/_document.tsx`:
```tsx
<body>
  <Main />
  <NextScript />
  <script dangerouslySetInnerHTML={{__html: `window.__IA_SUPPORT_CTA_URL__ = 'https://support.innovativeautomations.dev/';`}} />
  <script defer src="/ia-support-cta.js"></script>
</body>
```

**React (CRA/Vite)** - `public/index.html`:
```html
<body>
  <div id="root"></div>
  <script>window.__IA_SUPPORT_CTA_URL__ = 'https://support.innovativeautomations.dev/';</script>
  <script defer src="/ia-support-cta.js"></script>
</body>
```

**Vue** - `public/index.html`:
```html
<body>
  <div id="app"></div>
  <script>window.__IA_SUPPORT_CTA_URL__ = 'https://support.innovativeautomations.dev/';</script>
  <script defer src="/ia-support-cta.js"></script>
</body>
```

**Static HTML** - Before `</body>`:
```html
  <script>window.__IA_SUPPORT_CTA_URL__ = 'https://support.innovativeautomations.dev/';</script>
  <script defer src="/ia-support-cta.js"></script>
</body>
```

### Step 3: Add README Section
```markdown
## 🤝 Support CTA

This project includes a "Support & Build With Us" button linking to our support hub.

**Override URL:** Set `IA_SUPPORT_CTA_URL` environment variable
**Disable:** Set `IA_SUPPORT_CTA_DISABLE=true`
```

---

## ✅ Testing Checklist

- [ ] Button appears bottom-right corner
- [ ] Clicking opens https://support.innovativeautomations.dev/ in new tab
- [ ] Tab key navigation works (keyboard accessible)
- [ ] Dark/light mode switches colors correctly
- [ ] No overlap with existing UI elements
- [ ] Mobile responsive (test on phone)

---

## 📝 Commit Message Template

```
feat: add universal "Support & Build With Us" floating CTA

- Add configurable support CTA button (bottom-right)
- Links to https://support.innovativeautomations.dev/
- Configurable via IA_SUPPORT_CTA_URL env variable
- Fully accessible (keyboard, screen readers)
- Auto dark/light mode support
- Can disable via IA_SUPPORT_CTA_DISABLE=true
```

---

## 🚨 Special Cases

**Streamlit Apps** - Use inline HTML in Python:
```python
st.markdown('<a href="https://support.innovativeautomations.dev/" class="ia-cta">Support & Build With Us</a>', unsafe_allow_html=True)
```

**CLI Tools** - Skip (no web UI)

---

## 📊 Progress Tracker (Top 8)

| Done | Site | Repo |
|------|------|------|
| ⬜ | faithandpolicy.com | biblical-political-analyzer |
| ⬜ | placementsproposal.com | placement-investment-proposal |
| ⬜ | lido-partnership-proposal.netlify.app | lido-proposal |
| ⬜ | visa-glow-tool.netlify.app | visa-glow-tool |
| ⬜ | spaces-by-premier.netlify.app | spaces-by-premier |
| ⬜ | evaluation-tool-jacksonwink.netlify.app | evaluation-tool-jacksonwink |
| ⬜ | p2025-theta.vercel.app | p2025 |
| ⬜ | multi-brand-email-automation.netlify.app | multi-brand-email-automation |

---

## ⏱️ Time Estimate

**Per site:** 20-30 minutes
**Top 8 sites:** 3-4 hours total

---

## 🎯 Goal

Add subtle, accessible support button to all live sites without disrupting existing design or functionality.

**Questions?** See full brief: `DEVELOPER_CTA_IMPLEMENTATION_BRIEF.md`
