# Privacy Policy for Morpho on Apple TV

**Last Updated:** September 29, 2026

## 1. Overview

Morpho on Apple TV (“Morpho” or “the App”) is a media client developed by Mahmoud Abdel-Hafiz. This policy describes the Apple TV app. The [iPhone and iPad privacy policy](README.md) describes those versions separately.

The Apple TV app does not require a Morpho account or Sign in with Apple. The developer does not operate a central Morpho watch-history server, sell personal information, or use your media activity for advertising or cross-app tracking. Information can still leave your device when the app accesses iCloud, configured sources, metadata, artwork, media, or subtitles.

## 2. Contact

**Developer / privacy contact:** Mahmoud Abdel-Hafiz  
**Email:** [MHafiz0898@gmail.com](mailto:MHafiz0898@gmail.com)

Use this address for questions about this policy or information held by the developer. Requests concerning Apple or a media provider may also require that provider’s controls.

## 3. Data on Your Apple TV

Morpho stores source configurations and selected imported data in local app preferences. Source configurations include endpoint URLs and manifests describing catalogs, metadata, streams, and subtitles. URLs can contain tokens or other private configuration.

Playback history includes media identifiers, titles, artwork URLs, episode information, playback positions, durations, and last-watched timestamps. The app uses this information for Continue Watching and watched status. It also stores playback preferences, such as audio and subtitle choices and remembered audio tracks.

Artwork, metadata, stream results, and downloaded subtitle data may be cached to support browsing and playback. Some caches are held in memory; system networking and player components may also cache data.

The TMDB API key imported from iCloud is stored locally using Apple’s Keychain. This does not mean that copies in iCloud, source URLs, or other app preferences receive the same protection.

## 4. iCloud and the Companion App

The Apple TV app reads Apple’s iCloud key-value storage associated with Morpho. This can import source configurations and their enabled or disabled states, watch history, saved library items, cached Trakt list items, and a TMDB API key previously made available by the companion app.

Sync can occur at launch, when returning to the app, during refreshes, when iCloud reports a change, or through **Settings → Sync from iPhone**. It uses the Apple account configured on your device and depends on compatible data being available in the shared iCloud storage.

The current Apple TV implementation reads this key-value storage rather than the iPhone app’s separate CloudKit sync record or iCloud Drive backup files. Data in those other locations is not automatically interchangeable with this sync path.

Playback progress created on Apple TV is saved locally. The current TV implementation does not upload that progress to the shared iCloud store. A later import of companion-app history can replace the locally stored history. Do not assume that watch progress is synchronized in both directions.

Apple handles iCloud information under its own privacy practices. Source URLs and API keys in shared key-value storage are not described here as separately encrypted by Morpho.

## 5. Network Requests and Providers

Services contacted by Morpho receive your IP address and technical request information, including an Apple TV browser-style User-Agent for source requests. Providers may log and retain these requests under their own policies. Requests may occur automatically while browsing or loading artwork, as well as when you search or play media.

- **Configured sources and Stremio-compatible endpoints:** Catalog, search, metadata, stream, and subtitle requests can include search terms, media identifiers, season and episode information, and credentials embedded in a configured URL.
- **Media and subtitle hosts:** The player accesses the selected media URL, and subtitle features retrieve selected subtitle files. These hosts receive the requested URLs and any credentials or request headers needed to access them.
- **Metadata and artwork providers:** Source metadata services, including Cinemeta when configured, receive relevant lookups. TMDB requests send the configured API key and media identifiers or titles used for artwork and cast lookups. Artwork URLs supplied by sources can lead to other image hosts.
- **IntroDB and TheIntroDB:** When intro skipping is enabled for supported episodes, lookups send the media identifier and season and episode numbers to retrieve segment timings.

Trakt list items imported through iCloud may be displayed locally. This policy does not describe the Apple TV app as directly signing in to Trakt or sending TV playback events to Trakt.

The developer does not control independently operated source, media, subtitle, or artwork services. Consult their privacy information before using them.

## 6. Retention and Controls

Local data remains until changed, removed, or cleared by the app or operating system. Artwork and other caches can be recreated when you browse again. Watched-status controls can remove supported entries from local playback history.

Manage the original source configurations and shared cloud information through the companion app and applicable Apple controls. Changes in iCloud do not necessarily erase previously imported local copies immediately. Disconnecting a source or removing its configuration does not necessarily invalidate a token; revoke authorization with its provider when needed.

Removing the Apple TV app does not delete shared iCloud data, companion-app data, provider-held records, or exported configurations. Keychain entries may also remain. Reinstalling or syncing can import available cloud information again.

The current Apple TV Settings screen does not offer an account-deletion or comprehensive cloud-deletion control. There is no Morpho account to delete. Cloud copies and separate backups must be managed through the applicable companion-app or Apple controls.

## 7. Diagnostics and Support

Crash reports and TestFlight feedback made available through Apple depend on Apple’s reporting features and settings. Such reports and attachments can contain device, diagnostic, or identifying information.

If you contact the developer, the developer receives your email address, message, and attachments and uses them to respond and investigate. Avoid sharing passwords, API keys, tokens, or private source URLs. Support correspondence and submitted diagnostics are retained as needed to address the request and meet applicable obligations.

## 8. Security and Sharing

Morpho uses Apple’s app sandbox and Keychain for the TMDB key described above. Network protection depends on the endpoint: configured source or media URLs may use HTTP. The app does not guarantee that every connection or stored configuration is encrypted.

Protect your Apple account, Apple TV, and configured source URLs. No storage or transmission method is completely secure.

The developer does not sell or rent personal information or share it for advertising profiles. Connected providers receive information needed for the features described above. Information held by the developer may be disclosed where required by law or necessary to address security, abuse, or legal claims.

## 9. Privacy Rights and Third Parties

Depending on your location and applicable law, you may have rights to access, correct, delete, or obtain a copy of personal information, or object to or restrict its processing. Contact the developer regarding information the developer holds. On-device, Apple-held, and independently provider-held information may require their respective controls; the developer cannot directly erase every provider’s records.

Apple and other providers may process information outside your country under their own policies and safeguards.

See [Apple’s privacy policy](https://www.apple.com/legal/privacy/) and [TMDB’s privacy policy](https://www.themoviedb.org/privacy-policy). For Cinemeta, IntroDB, TheIntroDB, and configured source, stream, subtitle, and artwork hosts, consult the relevant operator’s privacy information.

## 10. Children and Policy Changes

Morpho is not intended for children under 16. If you believe a child has sent personal information to the developer, contact the address above so it can be addressed and deleted where appropriate.

This policy may change as the Apple TV app’s features or data handling change. The date above identifies the revision.
