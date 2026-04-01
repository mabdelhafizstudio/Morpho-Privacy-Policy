# Privacy Policy for Morpho: Content Hub

**Last Updated:** April 1, 2026

## Summary of Data Practices

Morpho is designed to minimize collection of personal data and contains **no tracking, advertising, analytics, or profiling**.

| Category                     | Collected?          | Notes                                                  |
| ---------------------------- | ------------------- | ------------------------------------------------------ |
| Personal Identifiers         | No                  | None                                                   |
| Location Data                | No                  | None                                                   |
| Device or Usage Analytics    | No                  | Only optional anonymized crash reports via Apple       |
| Advertising / Marketing      | No                  | None                                                   |
| Third-Party API Credentials  | Yes (user-provided) | Stored securely on-device or encrypted in CloudKit     |
| Watch History & Library Data | Yes (optional)      | Local or encrypted iCloud sync at user’s choice        |
| AI Chat History (Morpho AI)  | Yes (optional)      | Local + optional encrypted sync; fully user-controlled |

## 1. Introduction

Welcome to Morpho: Content Hub (“Morpho,” “the App”). This Privacy Policy explains how Morpho handles information, including personal data, in connection with the operation of the App. Morpho is committed to protecting user privacy and complying with applicable data protection laws, including the EU General Data Protection Regulation (GDPR). It also describes how Morpho meets Apple App Store privacy requirements. Please read this policy carefully.

## 2. Data Controller / Contact Information

**Data Controller:** Mahmoud Abdel-Hafiz (individual developer of Morpho)  
**Contact Email:** MHafiz0898@gmail.com

For any privacy inquiries or requests, please use the email address above. A physical postal address is not published. An electronic contact address is sufficient under GDPR Article 13 to enable data subjects to exercise their rights. If a competent supervisory authority formally determines that a physical address is required, the developer will provide it confidentially to that authority without delay.

## 3. Information Morpho Handles

Morpho is designed to minimize direct collection of personal data. To provide its services, Morpho handles the following information:

### Authentication & Third-Party Service Credentials

To connect with services at the user’s explicit request, Morpho may require API keys, OAuth tokens, or authentication credentials. This includes:

- Trakt: OAuth token stored securely in the device Keychain
- TMDB: API key stored in encrypted CloudKit fields
- Anthropic (Claude): API key stored in encrypted CloudKit fields (optional, for Morpho AI)
- xAI (Grok): API key stored in encrypted CloudKit fields (optional, for Morpho AI)
- Plex, Jellyfin, WebDAV, Dropbox: connection credentials stored in the device Keychain or encrypted local storage

All sensitive credentials are stored using Apple’s iOS Keychain or CloudKit’s encryptedValues API. Morpho never stores passwords or API keys in plain text.

### iCloud / CloudKit Sync Data

If the user enables iCloud Sync, certain app data (watch history, library items, addon configurations, collections, and preferences) is synced via the user’s private CloudKit database. Sensitive fields such as API keys use CloudKit’s encryptedValues API (end-to-end encrypted and inaccessible to the developer). This data is subject to Apple’s iCloud terms and privacy policy.

### Stremio Addon-Related Information

When users install and use third-party Stremio addons from user-provided URLs, Morpho interacts with the addon’s specified server endpoint at the user’s direction. Morpho may send content identifiers (such as IMDb or TMDB IDs) or user-initiated queries to the addon’s URL. Addon providers are independent data controllers. Users should review the privacy information provided by each addon provider.

### Morpho AI (Optional Feature)

Morpho AI is an optional AI-powered recommendation feature. When enabled, it uses the user’s own API key (Anthropic’s Claude or xAI’s Grok) to generate movie and TV recommendations. User messages and relevant media metadata are sent to the chosen AI provider. No device data, location, or other personal identifiers are included. AI chat history is stored locally on the device and optionally synced via CloudKit. The user can clear the history at any time in Settings. Morpho AI is completely optional; all other features work without it.

### Crash and Diagnostic Reports

With the user’s consent (via iOS analytics sharing or TestFlight), anonymized crash reports containing technical details (error codes, app version, device model, iOS version) may be sent to Apple and made available to the developer. These reports do not include personal data.

### No Tracking or Advertising

Morpho does not collect or transmit any user data for analytics, profiling, advertising, or marketing purposes. There are no third-party trackers, ad SDKs, or analytics tools in the app.

## 4. Legal Basis for Processing (GDPR)

- **Consent** (Art. 6(1)(a)): Storing user-provided credentials, enabling iCloud Sync, using Morpho AI, and using specific Stremio addons.
- **Contract Performance** (Art. 6(1)(b)): Sending requests to user-connected services (Trakt, TMDB, Plex, Jellyfin, etc.) to deliver core functionality.
- **Legitimate Interests** (Art. 6(1)(f)): Storing local app configuration, implementing security measures for credentials, and processing anonymized crash reports to improve stability.

All personal data processing is optional. Declining to provide credentials or enabling optional features only limits those specific integrations.

## 5. How Morpho Uses Information

Morpho uses information strictly to provide the app’s functionality:

- Streaming, library, and metadata features via user-configured sources
- Cross-device sync via CloudKit (when enabled)
- AI-powered recommendations via Morpho AI (when enabled)
- Secure storage of credentials
- Diagnosis of technical issues via anonymized crash reports

## 6. Data Sharing and Disclosure

Morpho does not sell, rent, or share personal information for commercial purposes.

Data is transmitted to third-party services **only at the user’s direction**:

- Apple (iCloud, Sign in with Apple, crash reports)
- Trakt, TMDB, Plex, Jellyfin, Dropbox, Anthropic, xAI (links to their privacy policies are provided in section 11)
- User-installed Stremio addons
- Intro skip services (IntroDB / TheIntroDB): only anonymous content identifiers (IMDb IDs, season/episode numbers)

**California Privacy Rights (CCPA/CPRA):** Morpho does not sell or share personal information as defined under California law. We do not engage in cross-context behavioral advertising.

Legal disclosure may occur if required by law or to protect the rights, property, or safety of users or the developer.

## 7. Data Retention

- Locally stored credentials and data remain until removed by the user or the app is uninstalled.
- CloudKit synced data follows Apple’s iCloud retention policies and can be deleted by the user via iCloud settings.
- AI chat history can be cleared anytime in Settings.
- Morpho does not operate its own servers or maintain a central user database.

## 8. User Rights (GDPR)

You have the right to:

- Access, rectify, or erase your personal data
- Restrict or object to processing
- Data portability
- Withdraw consent at any time

To exercise these rights, contact: **MHafiz0898@gmail.com**. We will respond within one month.

You may also lodge a complaint with your local supervisory authority (see European Data Protection Board directory).

Morpho does not engage in automated decision-making or profiling (GDPR Art. 22).

## 9. Data Security

- Sensitive credentials use Apple’s iOS Keychain
- CloudKit sensitive fields use end-to-end encryption (encryptedValues API)
- All external communications use HTTPS/TLS
- Minimal data transmission principle

## 10. International Data Transfers

When you direct Morpho to connect to third-party services located outside the EEA, data may be transferred under GDPR Article 49 (user-directed necessity). All transfers occur over encrypted connections. Please review the privacy policies of each service for their transfer practices.

## 11. Third-Party Services

- [Apple](https://www.apple.com/legal/privacy/)
- [Trakt](https://trakt.tv/privacy)
- [TMDB](https://www.themoviedb.org/privacy-policy)
- [Anthropic (Claude)](https://www.anthropic.com/privacy)
- [xAI (Grok)](https://x.ai/privacy)
- [Plex](https://www.plex.tv/about/privacy-center/)
- [Dropbox](https://www.dropbox.com/privacy)
- Others (Jellyfin is self-hosted; Stremio addons are user-controlled)

## 12. App Store and Platform Compliance

Morpho’s App Store privacy label and Privacy Manifest accurately reflect these practices. iCloud sync uses private databases with end-to-end encryption for sensitive fields. Sign in with Apple provides only a display name and identifier.

## 13. Children’s Privacy

Morpho is not intended for children under 16. We do not knowingly collect personal information from children. Contact MHafiz0898@gmail.com if you believe a child has provided data, and we will delete it promptly.

## 14. Changes to This Privacy Policy

We may update this policy to reflect new features or legal requirements. The “Last Updated” date shows the revision date. Continued use after changes constitutes acceptance.

If you have any questions, please contact: **MHafiz0898@gmail.com**
