# 🎯 Developer Brief: Support CTA Implementation Across All Repos

**Date:** November 4, 2025
**Project:** IGTA-Tech Universal Support CTA Button
**Priority:** HIGH - Live Production Sites First

---

## 📋 Executive Summary

Add a floating "Support & Build With Us" CTA button to all live websites and applications. Button must be:
- Fixed bottom-right corner
- Minimal, accessible, non-intrusive
- Consistent across all tech stacks
- Configurable via environment variables

**Default URL:** `https://support.innovativeautomations.dev/`
**Fallback URL:** `https://linktr.ee/innovativeautomations`

---

## 🎨 Design Requirements

### Visual Specifications
- **Position:** Fixed bottom-right, `bottom: 20px`, `right: 20px`, `z-index: 99999`
- **Style:** Rounded pill, subtle shadow, minimum 44×44px touch area
- **Label:** "Support & Build With Us"
- **Colors:** Auto dark/light mode support via CSS variables
- **Accessibility:** Keyboard accessible, `aria-label`, focus states
- **Motion:** Respect `prefers-reduced-motion`

### Collision Detection
- Detect cookie banners, chat widgets: `[data-cookie-banner]`, `.cookie`, `.cc-window`, `.chat-widget`
- If found, add extra offset: `bottom: 72px`

### Configuration
- **Primary:** `IA_SUPPORT_CTA_URL` env variable
- **Disable:** `IA_SUPPORT_CTA_DISABLE=true` to skip rendering
- **JavaScript Override:** `window.__IA_SUPPORT_CTA_URL__`

---

## 📊 Repository Implementation List (Ranked by Priority)

### 🔴 TIER 1: LIVE PRODUCTION WITH CUSTOM DOMAINS (HIGHEST PRIORITY)

#### 1. Biblical Political Analyzer
- **GitHub:** https://github.com/IGTA-Tech/biblical-political-analyzer
- **Live URL:** https://faithandpolicy.com
- **Status:** ✅ Production, 🔒 Private Repo
- **Tech Stack:** [NEEDS INVESTIGATION]
- **Last Updated:** 2025-10-28
- **Notes:** Real-time biblical perspectives analyzer
- **Priority Level:** 🔴 CRITICAL

#### 2. Placement Investment Proposal
- **GitHub:** https://github.com/IGTA-Tech/placement-investment-proposal
- **Live URL:** https://placementsproposal.com
- **Status:** ✅ Production, 🔒 Private Repo
- **Tech Stack:** Investment proposal site with Claude chat function
- **Last Updated:** 2025-10-24
- **Priority Level:** 🔴 CRITICAL

---

### 🟠 TIER 2: LIVE PRODUCTION ON NETLIFY/VERCEL (HIGH PRIORITY)

#### 3. LIDO Partnership Proposal
- **GitHub:** https://github.com/IGTA-Tech/lido-proposal
- **Live URL:** https://lido-partnership-proposal.netlify.app
- **Status:** ✅ Production, 🌐 Public
- **Tech Stack:** [NEEDS INVESTIGATION - likely React/Next.js]
- **Last Updated:** 2025-10-31
- **Notes:** 91% CAC reduction strategy proposal
- **Priority Level:** 🟠 HIGH

#### 4. Visa Glow Tool
- **GitHub:** https://github.com/IGTA-Tech/visa-glow-tool
- **Live URL:** https://visa-glow-tool.netlify.app
- **Status:** 🚧 Development, 🔒 Private Repo
- **Tech Stack:** Next.js
- **Last Updated:** 2025-10-30
- **Priority Level:** 🟠 HIGH

#### 5. Multi-Brand Email Automation
- **GitHub:** https://github.com/IGTA-Tech/multi-brand-email-automation
- **Live URL:** https://multi-brand-email-automation.netlify.app
- **Status:** 🚧 Development, 🌐 Public
- **Tech Stack:** [NEEDS INVESTIGATION]
- **Last Updated:** 2025-10-22
- **Priority Level:** 🟠 HIGH

#### 6. Spaces by Premier
- **GitHub:** https://github.com/IGTA-Tech/spaces-by-premier
- **Live URL:** https://spaces-by-premier.netlify.app
- **Status:** ✅ Production, 🌐 Public
- **Tech Stack:** Event venue booking system
- **Last Updated:** 2025-10-21
- **Notes:** Smart Inquiry Management System prototype
- **Priority Level:** 🟠 HIGH

#### 7. Evaluation Tool - Jackson Wink
- **GitHub:** https://github.com/IGTA-Tech/evaluation-tool-jacksonwink
- **Live URL:** https://evaluation-tool-jacksonwink.netlify.app
- **Status:** 🚧 Development, 🔒 Private Repo
- **Tech Stack:** [NEEDS INVESTIGATION]
- **Last Updated:** 2025-10-09
- **Priority Level:** 🟠 HIGH

#### 8. P2025 (Vercel)
- **GitHub:** https://github.com/IGTA-Tech/p2025
- **Live URL:** https://p2025-theta.vercel.app
- **Status:** ✅ Production, 🌐 Public
- **Tech Stack:** [NEEDS INVESTIGATION - likely Next.js on Vercel]
- **Last Updated:** 2025-09-30
- **Priority Level:** 🟠 HIGH

---

### 🟡 TIER 3: STAGING SITES (MEDIUM PRIORITY)

#### 9. IAS Investment Proposal (General)
- **GitHub:** https://github.com/IGTA-Tech/ias-investment-proposal-general
- **Live URL:** https://ias-investment-proposal-general.netlify.app
- **Status:** 🧪 Staging, 🔒 Private Repo
- **Tech Stack:** [NEEDS INVESTIGATION]
- **Last Updated:** 2025-10-24
- **Priority Level:** 🟡 MEDIUM

#### 10. IAS Investment Proposal V2
- **GitHub:** https://github.com/IGTA-Tech/ias-investment-proposal-v2
- **Live URL:** https://ias-investment-proposal-v2.netlify.app
- **Status:** 🧪 Staging, 🔒 Private Repo
- **Tech Stack:** [NEEDS INVESTIGATION]
- **Last Updated:** 2025-10-24
- **Priority Level:** 🟡 MEDIUM

#### 11. IAS Investment Proposal (Main)
- **GitHub:** https://github.com/IGTA-Tech/ias-investment-proposal
- **Live URL:** https://ias-investment-proposal.netlify.app
- **Status:** ✅ Production, 🔒 Private Repo
- **Tech Stack:** Interactive 250K seed round proposal
- **Last Updated:** 2025-10-24
- **Notes:** Has staging designation but marked as production
- **Priority Level:** 🟡 MEDIUM

---

### 🟢 TIER 4: PRODUCTION APPS WITHOUT LIVE URLS (LOWER PRIORITY)

#### 12. Innovative Automations PPM Builder
- **GitHub:** https://github.com/IGTA-Tech/innovative-automations-ppm-builder
- **Live URL:** N/A
- **Status:** ✅ Production, 🌐 Public
- **Tech Stack:** AI-Powered Private Placement Memorandum Builder SaaS
- **Last Updated:** 2025-11-03
- **Notes:** Full production SaaS platform
- **Priority Level:** 🟢 LOWER (No live deployment yet)

#### 13. Car Speed Analyzer Ultimate
- **GitHub:** https://github.com/IGTA-Tech/car-speed-analyzer-ultimate
- **Live URL:** N/A
- **Status:** ✅ Production, 🌐 Public
- **Tech Stack:** Educational app for kids
- **Last Updated:** 2025-11-02
- **Priority Level:** 🟢 LOWER

#### 14. Speedcards
- **GitHub:** https://github.com/IGTA-Tech/speedcards
- **Live URL:** N/A
- **Status:** ✅ Production, 🌐 Public
- **Tech Stack:** Interactive card-based speed learning game
- **Last Updated:** 2025-11-02
- **Priority Level:** 🟢 LOWER

#### 15. FMC Praise Team
- **GitHub:** https://github.com/IGTA-Tech/fmc-praise-team
- **Live URL:** N/A
- **Status:** ✅ Production, 🌐 Public
- **Tech Stack:** Worship schedule management with Google Sheets backend
- **Last Updated:** 2025-11-02
- **Priority Level:** 🟢 LOWER

#### 16. SSV Content Generator
- **GitHub:** https://github.com/IGTA-Tech/ssv-content-generator
- **Live URL:** N/A
- **Status:** ✅ Production, 🌐 Public
- **Tech Stack:** Automated blog content for Sherrod Sports Visas - v6.0
- **Last Updated:** 2025-10-30
- **Priority Level:** 🟢 LOWER

#### 17. Business Fraud Investigation System
- **GitHub:** https://github.com/IGTA-Tech/business-fraud-investigation-system
- **Live URL:** N/A
- **Status:** ✅ Production, 🔒 Private Repo
- **Tech Stack:** AI-powered BI analyzing 20+ data sources
- **Last Updated:** 2025-10-30
- **Priority Level:** 🟢 LOWER

#### 18. Investigator AI
- **GitHub:** https://github.com/IGTA-Tech/investigator-ai
- **Live URL:** N/A
- **Status:** ✅ Production, 🌐 Public
- **Tech Stack:** AI-powered business intelligence platform
- **Last Updated:** 2025-10-29
- **Priority Level:** 🟢 LOWER

#### 19. Landing Page Generator
- **GitHub:** https://github.com/IGTA-Tech/landing-page-generator
- **Live URL:** N/A (Streamlit App)
- **Status:** ✅ Production, 🌐 Public
- **Tech Stack:** **Streamlit** - AI landing page generator with Claude & DALL-E
- **Last Updated:** 2025-10-24
- **Notes:** ⚠️ Streamlit apps require different approach
- **Priority Level:** 🟢 LOWER

#### 20. Multi-Brand Email Automation IGTA
- **GitHub:** https://github.com/IGTA-Tech/multi-brand-email-automation-igta
- **Live URL:** N/A
- **Status:** ✅ Production, 🌐 Public
- **Tech Stack:** Email automation with AI personalization
- **Last Updated:** 2025-10-22
- **Priority Level:** 🟢 LOWER

#### 21. Claude-OpenAI Co-Project Tool
- **GitHub:** https://github.com/IGTA-Tech/Claude-OpenAI-Co-Project-Tool
- **Live URL:** N/A
- **Status:** ✅ Production, 🌐 Public
- **Tech Stack:** White-label AI platform with RAG and n8n
- **Last Updated:** 2025-10-22
- **Priority Level:** 🟢 LOWER

#### 22. InvestorBloc App
- **GitHub:** https://github.com/IGTA-Tech/investorbloc-app
- **Live URL:** N/A
- **Status:** ✅ Production, 🌐 Public
- **Tech Stack:** AI-Powered ROIC Analysis Platform with Claude AI
- **Last Updated:** 2025-10-17
- **Priority Level:** 🟢 LOWER

---

### ⚪ TIER 5: DEVELOPMENT/NO DEPLOYMENT (LOWEST PRIORITY)

#### 23. Website Scraper (Current Repo)
- **GitHub:** https://github.com/IGTA-Tech/website-scraper
- **Live URL:** N/A (CLI Tool)
- **Status:** 🚧 Development, 🌐 Public
- **Tech Stack:** **Python CLI** - AI-Powered Web Scraper
- **Last Updated:** 2025-11-04
- **Notes:** ⚠️ CLI tool, not web app. Skip or add to future web UI only.
- **Priority Level:** ⚪ SKIP FOR NOW

#### 24. Innovative Automations Investments
- **GitHub:** https://github.com/IGTA-Tech/innovative-automations-investments
- **Live URL:** N/A
- **Status:** 🚧 Development, 🔒 Private Repo
- **Tech Stack:** Investment documentation
- **Last Updated:** 2025-11-03
- **Priority Level:** ⚪ LOWEST

#### 25. Innovative Automations Investments Try 2
- **GitHub:** https://github.com/IGTA-Tech/innovative-automations-investments-try-2
- **Live URL:** N/A
- **Status:** 🚧 Development, 🔒 Private Repo
- **Tech Stack:** PPM references
- **Last Updated:** 2025-11-02
- **Priority Level:** ⚪ LOWEST

#### 26. FMC Chord Video
- **GitHub:** https://github.com/IGTA-Tech/FMC-chord-video
- **Live URL:** N/A
- **Status:** 🚧 Development, 🔒 Private Repo
- **Tech Stack:** Chord Video Generation System
- **Last Updated:** 2025-11-01
- **Priority Level:** ⚪ LOWEST

#### 27. Twitch Video Editor
- **GitHub:** https://github.com/IGTA-Tech/twitch-video-editor
- **Live URL:** N/A
- **Status:** 🚧 Development, 🌐 Public
- **Tech Stack:** [NEEDS INVESTIGATION]
- **Last Updated:** 2025-10-29
- **Priority Level:** ⚪ LOWEST

#### 28. Content Agent
- **GitHub:** https://github.com/IGTA-Tech/conent-agent
- **Live URL:** N/A
- **Status:** 🚧 Development, 🔒 Private Repo
- **Tech Stack:** Content agent JSON template workflows
- **Last Updated:** 2025-10-22
- **Priority Level:** ⚪ LOWEST

#### 29. Sherrod Sports Visas Lead App
- **GitHub:** https://github.com/IGTA-Tech/sherrod-sports-visas-lead-app
- **Live URL:** N/A
- **Status:** 🚧 Development, 🔒 Private Repo
- **Tech Stack:** Lead generation app
- **Last Updated:** 2025-10-08
- **Priority Level:** ⚪ LOWEST

---

### 🗑️ TIER 6: ARCHIVED (SKIP)

#### 30. OpenAI Codex
- **GitHub:** https://github.com/IGTA-Tech/openaicodex
- **Live URL:** N/A
- **Status:** 🗄️ Archived, 🔒 Private Repo
- **Tech Stack:** OpenAI Codex integration
- **Last Updated:** 2025-08-21
- **Priority Level:** ❌ SKIP (Archived)

---

## 🛠️ Implementation Instructions

### Step 1: Tech Stack Detection

For each repository, you need to:
1. Clone the repo
2. Identify the tech stack by checking:
   - `package.json` (React, Next.js, Vue, Angular, Svelte)
   - `requirements.txt` / `setup.py` (Django, Flask)
   - `Gemfile` (Rails)
   - `composer.json` (PHP/WordPress)
   - Static HTML files
3. Document findings before implementing

### Step 2: Create Universal JavaScript File

**File:** `public/ia-support-cta.js` (or appropriate path for stack)

```javascript
(function () {
  try {
    if (window.IA_SUPPORT_CTA_DISABLE === true || window.IA_SUPPORT_CTA_DISABLE === 'true') return;

    var href =
      window.__IA_SUPPORT_CTA_URL__ ||
      (typeof IA_SUPPORT_CTA_URL !== 'undefined' && IA_SUPPORT_CTA_URL) ||
      'https://support.innovativeautomations.dev/';

    if (typeof href !== 'string' || !/^https?:\/\//.test(href)) {
      href = 'https://support.innovativeautomations.dev/';
    }

    // Create style (skip if present)
    if (!document.getElementById('ia-cta-style')) {
      var style = document.createElement('style');
      style.id = 'ia-cta-style';
      style.textContent = `
:root {
  --ia-cta-bg: #111;
  --ia-cta-text: #fff;
  --ia-cta-radius: 9999px;
  --ia-cta-shadow: 0 6px 20px rgba(0,0,0,.15);
}
@media (prefers-color-scheme: dark) {
  :root { --ia-cta-bg: #fff; --ia-cta-text: #111; }
}
.ia-cta {
  position: fixed; bottom: 20px; right: 20px; z-index: 99999;
  display: inline-flex; align-items: center; justify-content: center;
  padding: 10px 14px; min-height: 44px; min-width: 44px;
  background: var(--ia-cta-bg); color: var(--ia-cta-text);
  border-radius: var(--ia-cta-radius); box-shadow: var(--ia-cta-shadow);
  font: 600 14px/1.1 system-ui, -apple-system, Segoe UI, Roboto, sans-serif;
  text-decoration: none; transition: transform .15s ease, box-shadow .15s ease;
}
@media (prefers-reduced-motion: reduce) {
  .ia-cta { transition: none; }
}
.ia-cta:focus, .ia-cta:hover { outline: none; transform: translateY(-1px); text-decoration: underline; }
.ia-cta:focus-visible { box-shadow: 0 0 0 3px rgba(99,102,241,.35), var(--ia-cta-shadow); }
      `;
      document.head.appendChild(style);
    }

    // Create anchor (skip if present)
    if (document.querySelector('.ia-cta')) return;

    var a = document.createElement('a');
    a.className = 'ia-cta';
    a.href = href;
    a.target = '_blank';
    a.rel = 'noopener noreferrer';
    a.setAttribute('aria-label', 'Support and build with us');
    a.textContent = 'Support & Build With Us';

    // Avoid overlap with cookie/chat widgets
    var extraBottom = 0;
    var blockers = document.querySelector('[data-cookie-banner], .cookie, .cc-window, .chat-widget');
    if (blockers) extraBottom = 52;
    a.style.bottom = (20 + extraBottom) + 'px';

    document.addEventListener('DOMContentLoaded', function () {
      document.body.appendChild(a);
    });
  } catch (e) {
    // fail silent
  }
})();
```

### Step 3: Framework-Specific Integration

#### A) Next.js / React (Most Common)

**Option 1: Using `app/layout.tsx` (App Router)**
```tsx
export default function RootLayout({ children }: { children: React.ReactNode }) {
  return (
    <html lang="en">
      <body>
        {children}

        {/* Support CTA Integration */}
        <script dangerouslySetInnerHTML={{__html: `
          window.__IA_SUPPORT_CTA_URL__ = '${process.env.IA_SUPPORT_CTA_URL ?? 'https://support.innovativeautomations.dev/'}';
        `}} />
        <script defer src="/ia-support-cta.js"></script>
      </body>
    </html>
  );
}
```

**Option 2: Using `pages/_document.tsx` (Pages Router)**
```tsx
import { Html, Head, Main, NextScript } from 'next/document'

export default function Document() {
  return (
    <Html lang="en">
      <Head />
      <body>
        <Main />
        <NextScript />

        {/* Support CTA Integration */}
        <script dangerouslySetInnerHTML={{__html: `
          window.__IA_SUPPORT_CTA_URL__ = '${process.env.IA_SUPPORT_CTA_URL ?? 'https://support.innovativeautomations.dev/'}';
        `}} />
        <script defer src="/ia-support-cta.js"></script>
      </body>
    </Html>
  )
}
```

**Option 3: Using `next/script` Component**
```tsx
import Script from 'next/script'

export default function RootLayout({ children }) {
  return (
    <html>
      <body>
        {children}

        <Script id="ia-cta-config" strategy="beforeInteractive">
          {`window.__IA_SUPPORT_CTA_URL__ = '${process.env.IA_SUPPORT_CTA_URL ?? 'https://support.innovativeautomations.dev/'}';`}
        </Script>
        <Script src="/ia-support-cta.js" strategy="lazyOnload" />
      </body>
    </html>
  )
}
```

#### B) Vue.js

**File:** `public/index.html` (Vue CLI) or `index.html` (Vite)
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <!-- ... -->
  </head>
  <body>
    <div id="app"></div>

    <!-- Support CTA Integration -->
    <script>
      window.__IA_SUPPORT_CTA_URL__ = '%VITE_IA_SUPPORT_CTA_URL%' || 'https://support.innovativeautomations.dev/';
    </script>
    <script defer src="/ia-support-cta.js"></script>
  </body>
</html>
```

**Environment:** `.env`
```
VITE_IA_SUPPORT_CTA_URL=https://support.innovativeautomations.dev/
```

#### C) Angular

**File:** `src/index.html`
```html
<!doctype html>
<html lang="en">
<head>
  <!-- ... -->
</head>
<body>
  <app-root></app-root>

  <!-- Support CTA Integration -->
  <script>
    window.__IA_SUPPORT_CTA_URL__ = '%IA_SUPPORT_CTA_URL%' || 'https://support.innovativeautomations.dev/';
  </script>
  <script defer src="assets/ia-support-cta.js"></script>
</body>
</html>
```

#### D) Static HTML

**Before `</body>` tag:**
```html
  <!-- Support CTA Integration -->
  <script>
    window.__IA_SUPPORT_CTA_URL__ = 'https://support.innovativeautomations.dev/';
  </script>
  <script defer src="/ia-support-cta.js"></script>
</body>
</html>
```

#### E) Django

**File:** `templates/base.html`
```html
<!DOCTYPE html>
<html>
<head>
  <!-- ... -->
</head>
<body>
  {% block content %}{% endblock %}

  <!-- Support CTA Integration -->
  <script>
    window.__IA_SUPPORT_CTA_URL__ = "{{ IA_SUPPORT_CTA_URL|default:'https://support.innovativeautomations.dev/' }}";
  </script>
  <script defer src="{% static 'js/ia-support-cta.js' %}"></script>
</body>
</html>
```

**Environment:** `settings.py`
```python
IA_SUPPORT_CTA_URL = os.getenv('IA_SUPPORT_CTA_URL', 'https://support.innovativeautomations.dev/')
```

#### F) Flask

**File:** `templates/base.html`
```html
<!DOCTYPE html>
<html>
<head>
  <!-- ... -->
</head>
<body>
  {% block content %}{% endblock %}

  <!-- Support CTA Integration -->
  <script>
    window.__IA_SUPPORT_CTA_URL__ = "{{ config.IA_SUPPORT_CTA_URL or 'https://support.innovativeautomations.dev/' }}";
  </script>
  <script defer src="{{ url_for('static', filename='js/ia-support-cta.js') }}"></script>
</body>
</html>
```

#### G) Streamlit (Special Case)

**File:** `app.py` (or main Streamlit file)
```python
import streamlit as st

# ... your Streamlit app code ...

# Support CTA Integration (at the bottom of the file)
st.markdown("""
<style>
:root {
  --ia-cta-bg: #111;
  --ia-cta-text: #fff;
  --ia-cta-radius: 9999px;
  --ia-cta-shadow: 0 6px 20px rgba(0,0,0,.15);
}
@media (prefers-color-scheme: dark) {
  :root { --ia-cta-bg: #fff; --ia-cta-text: #111; }
}
.ia-cta {
  position: fixed; bottom: 20px; right: 20px; z-index: 99999;
  display: inline-flex; align-items: center; justify-content: center;
  padding: 10px 14px; min-height: 44px; min-width: 44px;
  background: var(--ia-cta-bg); color: var(--ia-cta-text);
  border-radius: var(--ia-cta-radius); box-shadow: var(--ia-cta-shadow);
  font: 600 14px/1.1 system-ui, -apple-system, Segoe UI, Roboto, sans-serif;
  text-decoration: none; transition: transform .15s ease, box-shadow .15s ease;
}
.ia-cta:focus, .ia-cta:hover { outline: none; transform: translateY(-1px); text-decoration: underline; }
</style>

<a href="https://support.innovativeautomations.dev/" target="_blank" rel="noopener noreferrer" class="ia-cta" aria-label="Support and build with us">
  Support & Build With Us
</a>
""", unsafe_allow_html=True)
```

---

## 📝 Documentation Requirements

For each repository, add this section to the `README.md`:

```markdown
## 🤝 Support CTA

This project includes a "Support & Build With Us" floating button that links to our support hub.

### Configuration

**Default URL:** `https://support.innovativeautomations.dev/`

**Override the URL:**
```bash
# .env or environment variables
IA_SUPPORT_CTA_URL=https://linktr.ee/innovativeautomations
```

**Disable the button:**
```bash
IA_SUPPORT_CTA_DISABLE=true
```

### Customization

The button respects your design system via CSS variables:

```css
:root {
  --ia-cta-bg: #111;        /* Background color */
  --ia-cta-text: #fff;      /* Text color */
  --ia-cta-radius: 9999px;  /* Border radius */
  --ia-cta-shadow: 0 6px 20px rgba(0,0,0,.15); /* Box shadow */
}
```

The button automatically:
- Adapts to dark/light mode
- Avoids cookie banners and chat widgets
- Respects reduced-motion preferences
- Provides full keyboard accessibility
```

---

## ✅ Implementation Checklist (Per Repository)

- [ ] Clone repository
- [ ] Identify tech stack (check `package.json`, templates, etc.)
- [ ] Create `ia-support-cta.js` in appropriate directory
- [ ] Integrate script tags into root layout/template
- [ ] Add environment variable support (if applicable)
- [ ] Add README.md documentation section
- [ ] Test locally:
  - [ ] Button appears in bottom-right
  - [ ] Link works (opens in new tab)
  - [ ] Keyboard accessible (Tab key navigation)
  - [ ] Dark/light mode works
  - [ ] No conflicts with existing UI
- [ ] Commit with message: `feat: add universal "Support & Build With Us" floating CTA`
- [ ] Push to repository
- [ ] Verify on live deployment (if applicable)
- [ ] Document completion date and any issues

---

## 🚨 Special Considerations

### Private Repositories
- Ensure you have access before attempting to clone
- Some repos may require special authentication

### CLI/Backend-Only Tools
- **website-scraper** (Python CLI) - Skip for now unless adding web UI
- Any other CLI tools should be evaluated case-by-case

### Streamlit Apps
- Different approach required (see Streamlit section above)
- Cannot use external JS files
- Must use `st.markdown()` with inline HTML/CSS

### WordPress (if any exist)
- Add to theme's `functions.php`:
```php
add_action('wp_footer', function () {
  $url = getenv('IA_SUPPORT_CTA_URL') ?: 'https://support.innovativeautomations.dev/';
  echo "<script>window.__IA_SUPPORT_CTA_URL__ = '".esc_js($url)."';</script>\n";
  echo "<script defer src='".esc_url(get_stylesheet_directory_uri().'/ia-support-cta.js')."'></script>\n";
});
```

---

## 📊 Progress Tracking Template

Use this table to track implementation progress:

| # | Project Name | Tech Stack | Status | Deployed? | Completion Date | Notes |
|---|--------------|------------|--------|-----------|-----------------|-------|
| 1 | biblical-political-analyzer | TBD | ⏳ Pending | ✅ faithandpolicy.com | | |
| 2 | placement-investment-proposal | TBD | ⏳ Pending | ✅ placementsproposal.com | | |
| 3 | lido-proposal | TBD | ⏳ Pending | ✅ Netlify | | |
| ... | ... | ... | ... | ... | ... | ... |

**Status Legend:**
- ⏳ Pending
- 🔄 In Progress
- ✅ Complete
- ⚠️ Issues/Blocked
- ❌ Skipped

---

## 💰 Estimated Effort

**Per Repository:**
- Tech stack identification: 5-10 minutes
- File creation: 2-3 minutes
- Integration: 5-15 minutes (varies by stack)
- Testing: 5-10 minutes
- Documentation: 3-5 minutes
- **Total per repo:** ~20-40 minutes

**Total Project:**
- 8 Tier 1-2 repos (critical): ~4-6 hours
- 11 Tier 3-4 repos (medium): ~6-8 hours
- 9 Tier 5 repos (lower): ~3-5 hours
- **Grand Total:** ~13-19 hours

**Recommendation:** Start with Tier 1-2 (custom domains + live Netlify/Vercel sites) to get immediate value.

---

## 📞 Questions for Client Before Starting

1. **Access:** Do I have access to all private repositories? (11 private repos listed)
2. **Git Workflow:** Should I commit directly to `main` or create feature branches?
3. **Testing:** Should I test on staging/dev branches before production?
4. **Priorities:** Confirm Tier 1-2 should be done first?
5. **Special Cases:** Any repos that should be skipped or handled differently?
6. **Deployment:** Do you need deployment assistance after code changes?

---

## 🎯 Success Criteria

✅ Button appears on all live sites
✅ Links to correct URL (default: support.innovativeautomations.dev)
✅ Configurable via environment variables
✅ Accessible (keyboard, screen readers)
✅ Responsive (mobile, tablet, desktop)
✅ No visual conflicts with existing UI
✅ Documentation added to each README
✅ All changes committed with proper messages

---

**Document Version:** 1.0
**Last Updated:** November 4, 2025
**Contact:** [Your Contact Info]
**GitHub Organization:** https://github.com/IGTA-Tech
