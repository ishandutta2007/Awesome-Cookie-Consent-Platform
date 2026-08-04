# Awesome-Cookie-Consent-Platform

## Similar Projects to Cookie Consent Platforms

**Cookie Consent Platforms** (also called Consent Management Platforms or CMPs) help websites collect, store, and manage user consent for cookies and tracking technologies in compliance with GDPR, ePrivacy, CCPA/CPRA, and other privacy regulations. Leading commercial platforms include Cookiebot, Usercentrics, OneTrust, Didomi, Consentmanager, Osano, Iubenda, Termly, Crownpeak, and Complianz.

Below is a **curated list** of notable platforms and their open-source equivalents. The open-source CMP ecosystem offers several mature, self-hostable options that give full control over consent data and avoid third-party CDN dependency.

## 🏢 SaaS / Hosted Platforms

- **[Cookiebot](https://www.cookiebot.com/)** (by Usercentrics) — Popular CMP with automatic cookie scanning, consent logging, and strong compliance features for GDPR and other laws.
- **[Usercentrics](https://usercentrics.com/)** — Enterprise-grade consent management platform with advanced customization and multi-domain support.
- **[OneTrust](https://www.onetrust.com/)** — Comprehensive privacy and consent management suite widely used by large organizations.
- **[Didomi](https://www.didomi.io/)** — Modern CMP focused on consent, preference management, and compliance.
- **[Consentmanager](https://www.consentmanager.net/)** — Flexible consent management solution with multi-language and geo-targeting support.
- **[Osano](https://www.osano.com/)** — Privacy platform that includes consent management (also maintains a popular open-source cookie consent library).
- **[Iubenda](https://www.iubenda.com/)**, **[Termly](https://termly.io/)**, **[Crownpeak](https://www.crownpeak.com/)**, **[Complianz](https://complianz.io/)** — Widely used CMPs and privacy tools, especially popular with mid-market sites and WordPress users.

## 🔓 Open-Source Software

### Full / Self-Hosted Consent Management Platforms
- **[Klaro](https://github.com/kiprotect/klaro)** — Popular open-source (MIT) consent manager. Lightweight, highly customizable, supports granular categories, auto-blocking of scripts, and works well for GDPR compliance. Can be self-hosted with no external dependencies.
- **[c15t](https://github.com/c15t/c15t)** — Modern, developer-first open-source consent management framework. Framework-agnostic (React, Next.js, Vue, etc.), headless or with prebuilt UI, supports Google Consent Mode v2, IAB TCF, and full customization while keeping consent logic in your own stack.
- **[ConsentOS](https://github.com/consentos/consentos)** — Privacy-first, self-hosted cookie consent management platform positioned as an alternative to OneTrust, Cookiebot, and CookieYes. Includes banner, auto-blocking, scanning, compliance checks, and audit trails.
- **CookieConsent by Orestbida** and related modern JavaScript libraries — Accessible, customizable open-source consent banners with good documentation and active community use.

### Lightweight Open-Source Libraries & Widgets
- **[Osano Cookie Consent](https://github.com/osano/cookieconsent)** — One of the most widely used open-source JavaScript cookie consent libraries (MIT). Lightweight, free, and designed for GDPR, CCPA, and similar laws. The commercial Osano platform is separate.
- Community projects such as ConsentStack CMP, 68publishers consent tools, and various GTM-friendly cookie bars that provide banner + consent storage functionality.

### WordPress & Ecosystem Options
- Open-source or freemium WordPress plugins (e.g., Complianz free tier and similar community plugins) that keep consent data local and avoid heavy external SaaS dependency.
- Browser-side tools like Consent-O-Matic (open-source extension) that help users manage consents across sites.

### Typical Open-Source Approach
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
