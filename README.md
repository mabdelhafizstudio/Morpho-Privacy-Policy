# Privacy Policy for Morpho: Content Hub

**Last Updated:** September 29, 2026

## 1. Overview

Morpho: Content Hub (“Morpho” or “the App”) is a media player and library app developed by Mahmoud Abdel-Hafiz. This policy explains the information handled on your device and sent to Apple or other services when you use Morpho.

Morpho has no registration, Morpho login, or Sign in with Apple flow. It does not operate a central Morpho account or media-history server. Optional connections to services such as Plex, Jellyfin, and Trakt use those providers’ accounts. The developer does not sell personal information or use your media activity for advertising or cross-app tracking. This does not mean that no information leaves your device: connected services receive the requests needed to provide their features.

| Information | How Morpho handles it |
| --- | --- |
| Library, watch history, playback progress, collections, and preferences | Stored on-device; selected data can be copied to iCloud when you use sync or backup features |
| Service credentials and source configurations | Stored on-device; some credentials and configurations can be included in cloud sync, backups, or source exports |
| Local profile name | An optional display name is stored on-device; it does not create an account |
| Search terms, media identifiers, and file information | Used locally and sent to relevant metadata, source, subtitle, or connected-service endpoints as needed |
| Device and connection information | Connected services receive your IP address and request details; some integrations also receive a device or client identifier |
| Diagnostics and support messages | Local diagnostic logs; reports and feedback shared through Apple or sent by you may reach the developer |
| Precise location and biometric templates | Morpho does not request precise location or receive Face ID / Touch ID biometric templates |

## 2. Contact

**Developer / privacy contact:** Mahmoud Abdel-Hafiz  
**Email:** [MHafiz0898@gmail.com](mailto:MHafiz0898@gmail.com)

Contact this address with privacy questions or requests relating to information held by the developer. Information held by a connected service is also subject to that service’s privacy practices.

## 3. Information Stored on Your Device

### Library and playback

Morpho stores information needed to organize and play media, such as file names and paths, media identifiers and metadata, selected source folders and libraries, artwork, collections, watchlists, playback positions, watched status, and timestamps. It also caches artwork, thumbnails, catalogs, and metadata to improve loading.

Files you import and custom artwork you select are handled through the device’s file or photo-selection features. Media titles and related metadata may be indexed in the device’s Spotlight search. These features do not upload your entire photo library or media collection to the developer.

### Connections and credentials

Morpho stores server addresses, usernames, account or user identifiers, selected libraries, source URLs, API keys, and authentication tokens where needed for an integration.

Storage differs by feature. Trakt tokens, TMDB and OMDb API keys, and active Plex and Jellyfin tokens use Apple’s Keychain. Saved Jellyfin profiles include access tokens in locally stored profile data. Source URLs may themselves contain provider credentials or configuration values.

These distinctions also affect backups and cloud copies. Morpho does not promise that every credential is stored exclusively in the Keychain or protected by a separate app-level encryption layer.

### Local profile and removed sign-in

You may set a display name stored locally on your device. This is a local profile, not a Morpho account, and does not require an email address or password.

Sign in with Apple has been removed. When migrating from an older version, Morpho removes the locally stored Apple user identifier and email address. A previously entered custom name, or an older Apple-provided name when no custom name exists, can be retained as your local display name. Removing sign-in does not itself erase your library or existing cloud copies.

### App lock

The optional app lock uses Apple’s device authentication. Morpho receives an authentication result, not your biometric templates or device passcode.

## 4. iCloud Sync and Backups

Morpho offers separate CloudKit sync and iCloud Drive backup features. These use your Apple account and are governed by Apple’s terms and privacy policy.

**CloudKit sync:** Sync uses the iCloud account already configured on your device, without a separate Morpho sign-in. The iCloud Sync toggle defaults to on, but the current push and pull controls are manual. When you push data to iCloud, selected settings, source configurations, watch history, library items, collections, and connection information are stored in your private CloudKit database. The sync record also contains a device name, a device identifier, and modification information. Deletion records can contain item identifiers, deletion times, and the deleting device’s identifier.

The CloudKit implementation uses encrypted fields for designated sensitive settings and selected Keychain values. Other configurations are stored in ordinary CloudKit fields; these may include credentials embedded in source URLs or saved profiles. A private database is not a guarantee that every field has the same encryption protection.

**iCloud Drive backups:** When you create a file backup, Morpho writes a snapshot of selected settings, source configurations, history, saved library items, and selected credentials to a `.morphobackup` file. The file is JSON data without an additional app-provided encryption layer. Anyone with access to a backup file may be able to read its contents, including included credentials. Apple’s protection of the iCloud storage remains separate from this file format.

Older backup/sync paths also use Apple’s iCloud key-value storage for selected preferences and credentials. Morpho does not represent those copies as CloudKit encrypted fields. Existing backups may contain data from older app versions.

Apple’s protections depend on the iCloud service and your account settings. See [Apple’s iCloud data security overview](https://support.apple.com/en-us/102651) for details.

## 5. Connected Services and Network Requests

When Morpho contacts a service, that service receives your IP address and technical request information in addition to the data described below. It may retain server logs under its own policies. Some requests occur automatically while loading, refreshing, or prefetching catalogs and artwork, or during playback.

- **Plex and Jellyfin:** Requests authenticate your connection and browse or access your selected media, folders, libraries, artwork, and streams. They can disclose file paths, media identifiers, and requested content. Plex receives a persistent app-generated client identifier; Jellyfin requests include a device identifier and client information.
- **Trakt:** When connected, Morpho accesses profile and list information and can send playback start, pause, and stop events, content identifiers, episode numbers, and progress to your Trakt account.
- **TMDB, OMDb, Cinemeta, and artwork hosts:** Metadata and image requests may include searches, titles derived from filenames, media identifiers, and language or other lookup parameters. A configured API key is sent to its corresponding API. Artwork can also be requested from hosts such as MetaHub.
- **User-added sources and Stremio-compatible addons:** Morpho contacts configured endpoints for manifests, catalogs, searches, metadata, streams, and subtitles. Requests can include search terms, media identifiers, season/episode numbers, and provider-specific values included in the source URL. Stream and subtitle hosts receive requests when their content is accessed. An addon’s configuration page may load third-party web content governed by that provider.
- **IntroDB and TheIntroDB:** Intro-skip lookups send media identifiers and season/episode numbers to retrieve segment timing. These are network requests and are not guaranteed to be anonymous.
- **Google Cast:** When enabled and permitted, device discovery accesses the local network. Casting passes the selected stream URL, title, artwork URL, and playback information to the receiver through Google Cast. A stream URL may contain access credentials. Google Cast and the receiving device are subject to their providers’ privacy practices.
- **YouTube:** Trailer thumbnails may load from YouTube image servers. Opening a trailer sends you to YouTube or its app, where Google’s privacy practices apply.

**Demo Library:** The demo requires no service credentials or personal media server. It uses a curated catalog of public-domain titles, Cinemeta metadata, the Public Domain Movies endpoint at `caching.stremio.net`, and direct Internet Archive media links. Metadata, artwork, catalog, and playback requests reach those services and their delivery hosts, which receive your IP address and request details. The demo is therefore not an offline-only feature.

Demo library items, watch progress, and collections are kept in a temporary sandbox rather than your normal library. A local flag records whether the demo is active so it can resume after relaunch. Exiting returns to your normal configuration. Artwork and network caches may still be created while exploring the demo.

The current app no longer provides Morpho AI, Dropbox or WebDAV connections, or the previous offline download manager. It does not send recommendation chats to Anthropic or xAI. Upgrade cleanup removes supported obsolete local settings, credentials, caches, and app-managed download files, and filters retired settings from current CloudKit and file-backup restores. This does not guarantee removal of every older cloud snapshot, exported file, or provider-held record. Older copies remain subject to the retention and deletion distinctions in this policy.

## 6. Exports, Diagnostics, and Support

**Source exports:** Exporting or copying source configurations can include full addon URLs. These URLs may contain tokens or other private configuration. Review them before sharing; recipients and destinations you choose can access the exported data.

**Diagnostics:** Morpho writes local diagnostic information that can include errors, request URLs, server addresses, and media file names or paths. Reports made available through Apple’s diagnostics or TestFlight depend on Apple’s reporting features and applicable settings. Reports, screenshots, and beta feedback may contain information that identifies you or your content; they are not described here as invariably anonymous.

**Support:** If you email the developer, the developer receives your email address, message, and any attachments you send, and uses them to respond and investigate the issue. Avoid including passwords, tokens, or private source URLs.

## 7. Retention and Your Controls

Local information remains until removed, replaced, or cleared through the relevant app features. Cached content may be recreated when you use the app again.

- Remove history, library entries, collections, and sources using their respective controls. Disconnect services to remove their active local connection details; revoke authorization with the provider when you want to invalidate a token.
- Use **Settings → Data & Storage** to clear supported caches. Clearing caches is not the same as deleting your library, credentials, or cloud copies.
- Use the **iCloud Sync** screen’s **Delete Synced Data** action to delete the main CloudKit sync record and request cleanup of deletion records and legacy iCloud key-value data. Local data remains. Cloud deletion requires a successful connection and operation.
- Delete iCloud Drive backup snapshots separately through **iCloud Drive Backups** or your iCloud Drive files. The CloudKit deletion action does not delete those backup files.
- Turning off iCloud Sync does not erase existing cloud copies. Uninstalling the app removes its local app container, but Keychain entries, cloud data, exported files, and provider-held information may remain.
- Restoring or pushing data again can recreate copies. Data already sent to third parties is retained and deleted under their policies.

Cloud deletion markers are eligible for cleanup after 90 days during a subsequent push; this is best-effort cleanup, not a guaranteed deletion deadline. Support correspondence and shared diagnostics are retained as needed to address the request, investigate issues, and meet applicable obligations.

## 8. Security and Sharing

Morpho uses Apple’s app sandbox, Keychain for the credentials described above, and designated CloudKit encrypted fields. Network security depends on the endpoint: HTTPS is used by built-in public APIs, while user-configured sources and media URLs may use HTTP. Morpho therefore does not guarantee that every connection is encrypted.

No storage or transmission method is completely secure. Protect your device, Apple account, backup files, and configured source URLs.

The developer does not sell or rent personal information, share it for cross-context behavioral advertising, or use it for advertising profiles. Service providers receive information to perform the features described in this policy. Information held by the developer may also be disclosed where required by law or necessary to address security, abuse, or legal claims.

## 9. Privacy Rights and International Processing

Depending on your location and applicable law, you may have rights to access, correct, delete, or obtain a copy of personal information, restrict or object to processing, withdraw consent, or complain to a data-protection authority. Contact the developer to exercise applicable rights concerning information the developer holds.

Where data-protection law requires a legal basis, processing may be necessary to provide requested functionality, based on consent for optional processing where required, or based on legitimate interests in responding to support requests and protecting the app. Withdrawing consent does not affect processing that lawfully occurred before withdrawal.

Much of Morpho’s data is stored on your device or in your Apple account, so the relevant app, Apple, or connected-service controls may be necessary to complete a request. The developer cannot directly erase records held independently by every provider.

Apple and other connected providers may process information in countries outside your own. Their policies explain applicable transfer practices and safeguards. This policy does not assume that every transfer is covered by a single legal exception.

## 10. Third-Party Privacy Information

- [Apple](https://www.apple.com/legal/privacy/)
- [Trakt](https://trakt.tv/privacy)
- [TMDB](https://www.themoviedb.org/privacy-policy)
- [Plex](https://www.plex.tv/about/privacy-center/)
- [Google / YouTube / Google Cast](https://policies.google.com/privacy)
- [Internet Archive](https://archive.org/about/terms.php)

For OMDb, Cinemeta, MetaHub, IntroDB, TheIntroDB, addon endpoints, subtitle and stream hosts, and self-hosted Jellyfin servers, consult the relevant service or server operator’s privacy information. Morpho does not control their logging, retention, or subsequent use of information.

## 11. Children’s Privacy

Morpho is not intended for children under 16. The developer does not knowingly collect personal information from children. If you believe a child has sent personal information to the developer, contact the email above so the information can be addressed and deleted where appropriate.

## 12. Changes

This policy may be updated as Morpho’s features or data practices change. The “Last Updated” date identifies the revision. Any notice or consent required by applicable law will be handled separately.
