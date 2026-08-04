# Awesome-Cookie-Consent-Platform

<div align="center">
<img src="assets/banner.svg" alt="Awesome Cookie Consent Platform Banner">
</div>

## 🌟 Similar Projects to Cookie Consent Platforms

**Cookie Consent Platforms** (also called Consent Management Platforms or CMPs) help websites collect, store, and manage user consent for cookies and tracking technologies in compliance with GDPR, ePrivacy, CCPA/CPRA, and other privacy regulations. Leading commercial platforms include Cookiebot, Usercentrics, OneTrust, Didomi, Consentmanager, Osano, Iubenda, Termly, Crownpeak, and Complianz.

Below is a **curated list** of notable platforms and their open-source equivalents. The open-source CMP ecosystem offers several mature, self-hostable options that give full control over consent data and avoid third-party CDN dependency.

## 🏢 SaaS / Hosted Platforms 🚀

| Platform | Description | Pricing Tiers | Free Tier / Limits |
|----------|-------------|---------------|---------------------|
| **[Cookiebot](https://www.cookiebot.com/)** (by Usercentrics) | Popular CMP with automatic cookie scanning, consent logging, and strong compliance features for GDPR and other laws. | Free; Premium Lite from ~€7/mo; Premium Medium from ~€30/mo; Premium Large from ~€50/mo | ✅ Free: 1 domain, up to 50 subpages, no custom branding |
| **[Usercentrics](https://usercentrics.com/)** | Enterprise-grade consent management platform with advanced customization and multi-domain support. | Free; Essential from ~€7/mo; Pro from ~€30/mo; Business from ~€50/mo; Enterprise (custom) | ✅ Free: 1 domain, ~1,000 sessions/mo |
| **[OneTrust](https://www.onetrust.com/)** | Comprehensive privacy and consent management suite widely used by large organizations. | From ~$10,000/yr (modular, usage-based); Enterprise $50K–$300K+/yr — contact sales | ❌ No free tier |
| **[Didomi](https://www.didomi.io/)** | Modern CMP focused on consent, preference management, and compliance. | Essential / Advanced / Premium — all custom quote (contact sales) | ❌ No free tier |
| **[Consentmanager](https://www.consentmanager.net/)** | Flexible consent management solution with multi-language and geo-targeting support. | Free; Starter from €23/mo; Essential from €59/mo; Professional from €219/mo; Enterprise (custom) | ✅ Free: 1 domain, 5,000 pageviews/mo, Consentmanager branding |
| **[Osano](https://www.osano.com/)** | Privacy platform that includes consent management (also maintains a popular open-source cookie consent library). | Free; Plus from ~$199/mo; Enterprise (custom) | ✅ Free: 1 domain, 5,000 visitors/mo, basic banner only (no script-blocking) |
| **[Iubenda](https://www.iubenda.com/)** | Privacy and cookie compliance solution with policy generation and consent management. | Free; Essentials from ~€5/mo; Advanced (mid-tier); Ultimate up to ~€80/mo | ✅ Free: 1 website, limited pageviews, Iubenda branding |
| **[Termly](https://termly.io/)** | User-friendly CMP with auto cookie scanning and legal policy generators. | Free; Starter from ~$10/mo (annual); Pro+ from ~$15/mo (annual); Agency (custom) | ✅ Free: 1 website, 10,000 banner views/mo, quarterly scans, Termly watermark |
| **[Crownpeak](https://www.crownpeak.com/)** | Enterprise consent and tag governance platform (part of broader DXM suite). | Standard (custom); Enterprise (custom) — contact sales | ❌ No free tier |
| **[Complianz](https://complianz.io/)** | Popular WordPress-focused cookie consent plugin with compliance templates. | Free; Personal $59/yr (1 site); Professional $179/yr (5 sites); Agency $399/yr (25 sites) | ✅ Free WP plugin: unlimited sites, basic banner & scanning, no geo-detection/consent logging |

## 🔓 Open-Source Software 💻

### 🌐 Full / Self-Hosted Consent Management Platforms
- **[CookieConsent by Orestbida](https://github.com/orestbida/cookieconsent)** [![GitHub stars](https://img.shields.io/github/stars/orestbida/cookieconsent?style=social&color=white)](https://github.com/orestbida/cookieconsent/stargazers) and related modern JavaScript libraries — Accessible, customizable open-source consent banners with good documentation and active community use.
- **[c15t](https://github.com/c15t/c15t)** [![GitHub stars](https://img.shields.io/github/stars/c15t/c15t?style=social&color=white)](https://github.com/c15t/c15t/stargazers) — Modern, developer-first open-source consent management framework. Framework-agnostic (React, Next.js, Vue, etc.), headless or with prebuilt UI, supports Google Consent Mode v2, IAB TCF, and full customization while keeping consent logic in your own stack.
- **[Klaro](https://github.com/kiprotect/klaro)** [![GitHub stars](https://img.shields.io/github/stars/kiprotect/klaro?style=social&color=white)](https://github.com/kiprotect/klaro/stargazers) — Popular open-source (MIT) consent manager. Lightweight, highly customizable, supports granular categories, auto-blocking of scripts, and works well for GDPR compliance. Can be self-hosted with no external dependencies.
- **[ConsentOS](https://github.com/consentos/consentos)** [![GitHub stars](https://img.shields.io/github/stars/consentos/consentos?style=social&color=white)](https://github.com/consentos/consentos/stargazers) — Privacy-first, self-hosted cookie consent management platform positioned as an alternative to OneTrust, Cookiebot, and CookieYes. Includes banner, auto-blocking, scanning, compliance checks, and audit trails.

### ⚡ Lightweight Open-Source Libraries & Widgets
- **[Osano Cookie Consent](https://github.com/osano/cookieconsent)** [![GitHub stars](https://img.shields.io/github/stars/osano/cookieconsent?style=social&color=white)](https://github.com/osano/cookieconsent/stargazers) — One of the most widely used open-source JavaScript cookie consent libraries (MIT). Lightweight, free, and designed for GDPR, CCPA, and similar laws. The commercial Osano platform is separate.
- Community projects such as ConsentStack CMP, 68publishers consent tools, and various GTM-friendly cookie bars that provide banner + consent storage functionality.

### 🧩 WordPress & Ecosystem Options
- Open-source or freemium WordPress plugins (e.g., Complianz free tier and similar community plugins) that keep consent data local and avoid heavy external SaaS dependency.
- Browser-side tools like Consent-O-Matic (open-source extension) that help users manage consents across sites.

### 🛠️ Typical Open-Source Approach
1. **Consent banner & logic** — Klaro, c15t, or Osano Cookie Consent
2. **Auto-blocking of trackers** — Built-in script/cookie interception in the above tools
3. **Consent storage & audit** — Local storage + optional self-hosted backend (ConsentOS or custom)
4. **Integrations** — Google Consent Mode v2, GTM, and major analytics/ad pixels
5. **Hosting** — Fully first-party (your domain) to avoid CDN blocking and third-party data sharing

These solutions give website owners complete ownership of consent records, eliminate recurring per-pageview fees, and keep privacy infrastructure under their own control.

---

**How to contribute**  
Fork this repository, add a new project (with link + short description + category), and open a pull request.  
Prefer actively maintained open-source projects related to cookie consent, consent management platforms (CMPs), GDPR/CCPA compliance tools, or privacy preference centers.

**License**  
This list is public domain / CC0. Feel free to copy into your own awesome list or README.

Star the projects you find useful — open consent tools help websites stay compliant while respecting user privacy! 🍪
