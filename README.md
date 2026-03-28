# IntuneIPA Packager Pro

> Automates the entire iOS LOB app upload, versioning, and assignment workflow in Microsoft Intune so IT admins never touch the portal manually again.

## Overview

A PowerShell module and lightweight SaaS dashboard that takes a signed .ipa file, extracts metadata (bundle ID, version, display name), uploads it to Intune via the Graph API, auto-increments version tracking, and assigns it to specified Azure AD groups — all in one command or scheduled pipeline. It eliminates the tedious multi-step portal workflow and adds audit logging, version history, and rollback capabilities that Intune's native UI lacks.

## Problem This Solves

Manually uploading LOB .ipa files through the Intune portal is a slow, repetitive, error-prone process with no built-in version history, no rollback, and no CI/CD integration — causing deployment delays and configuration drift when teams update internal apps frequently

## Target Audience

IT admins and MSP consultants managing 200+ enrolled iOS devices for enterprise or regulated-industry clients (healthcare, finance, field services) who deploy internal LOB apps regularly

## Tech Stack

PowerShell, Microsoft Graph API, Next.js, Azure Functions, SQLite

## Installation

```powershell
# Clone the repository
git clone https://github.com/intune-ipa-packager-pro.git
cd intune-ipa-packager-pro

# Review the script before running
Get-Content scripts/intune-ipa-packager-pro.ps1

# Run with appropriate permissions
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
.\scripts\{intune-ipa-packager-pro}.ps1
```

## Usage

Accepts a local .ipa file path and target Azure AD group name, extracts app metadata via PList parsing, authenticates to Microsoft Graph, uploads the LOB app content, sets assignment to the specified group, and logs the version entry to a local JSON audit file.

## Monetization Strategy

PowerShell module sold as a one-time purchase at $49 (individual) or $149 (team/MSP license with 5 seats) via Gumroad or Lemon Squeezy; optional $19/month SaaS dashboard tier for version history, audit logs, and multi-tenant MSP support hosted as a lightweight web app

| Metric | Value |
|--------|-------|
| Revenue Potential | HIGH |
| Estimated Effort  | 1-3months |

## Contributing

1. Fork this repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'feat: add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

MIT License — see [LICENSE](LICENSE) for details.

---

*Generated from the article: [Add an iOS/iPadOS LOB App to Microsoft Intune](https://msendpoint.com/articles/add-an-ios-ipados-lob-app-to-microsoft-intune) on 2026-03-28*
*Blog: [MSEndpoint.com](https://msendpoint.com)*