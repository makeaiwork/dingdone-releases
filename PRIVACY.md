# DingDone Privacy Policy

**Effective date: July 15, 2026**

DingDone is a native macOS application operated by Denis Kazantsev ("DingDone", "we",
"us", or "our"). It speaks status notifications from supported coding agents and helps
you return to the project that needs your attention.

This Privacy Policy explains what information DingDone processes, why it is processed,
where it is stored, and the choices available to you. Questions and privacy requests can
be sent to [support@dingdone.io](mailto:support@dingdone.io).

## 1. The short version

- Apple system voices work locally on your Mac. Notification text is not sent to DingDone
  or a text-to-speech provider when you use an Apple voice.
- Premium voices are a cloud feature. When you select one, DingDone sends the short status
  phrase and voice settings through DingDone's server to Fish Audio for speech synthesis.
- DingDone does not send your source code, prompts, agent transcripts, or full agent
  messages to its licensing or text-to-speech servers.
- DingDone has no advertising SDK and does not sell personal information.
- The first public release does not provide a DingDone account or Cloud Sync. App settings,
  project names, favorites, widget settings, history, and audio cache remain on your Mac.
- Gumroad processes checkout, payment, receipts, refunds, subscriptions, and license-key
  issuance.

## 2. Information stored locally on your Mac

DingDone may store the following information in
`~/Library/Application Support/DingDone`:

- app, voice, phrase, project-name, widget, and agent-connection settings;
- your locally selected project names and favorites;
- a local event log and inbox containing timestamps, coding-agent name, a one-way session
  reference, project path, event type, and the short phrase spoken by DingDone;
- locally cached synthesized audio; and
- an offline entitlement projection used to decide which features are available.

The local event log rotates automatically after 4,000 lines and keeps the most recent 500
lines. Other local settings and cache files remain until you clear them or remove DingDone's
application-support data.

DingDone uses the macOS Data Protection Keychain for the license key, installation
identifier and token, entitlement integrity data, and the local Agent Cockpit trial receipt.
Keychain items may remain after the app itself is deleted. You can deactivate DingDone before
removing it or delete its Keychain items with macOS Keychain Access.

DingDone reads only the local coding-agent files and metadata needed to detect supported
events and open the relevant project or session. It does not upload agent transcripts,
prompts, responses, or source-code files to DingDone servers.

## 3. Purchases, licensing, and device activation

Purchases are made through Gumroad. Gumroad may provide DingDone with transaction and
license information needed to deliver and maintain your purchase, including:

- product, plan, sale, and subscription identifiers;
- purchase, cancellation, refund, dispute, and access status;
- the email address associated with the purchase; and
- the Gumroad license key you submit when activating the app.

DingDone uses this information to validate the purchase, activate up to two Macs, refresh
your entitlement, prevent fraud and abuse, handle refunds or disputes, and provide support.

The raw license key is sent during activation to the DingDone license service and Gumroad's
license-verification service. DingDone does not store the raw key in its server database. It
stores a keyed cryptographic lookup value instead. The raw purchase email is not stored in
the DingDone database; a normalized keyed lookup value is stored for support and entitlement
recovery. The raw license key remains in the app-only macOS Keychain on your Mac so the app
can refresh the license when required.

The DingDone license service also stores an installation identifier, user-provided device
label, app version, installation-token digest and version, entitlement state, safe audit
events, and the provider identifiers needed to reconcile the purchase. DingDone's text-to-
speech proxy does not receive your license key, purchase email, or Gumroad access token.

Gumroad handles payment-card and billing information. DingDone does not receive or store your
full payment-card number. Gumroad's processing is governed by the
[Gumroad Privacy Policy](https://gumroad.com/privacy).

## 4. Voice processing

### Apple system voices

When an Apple system voice is selected, speech synthesis happens locally through macOS.
DingDone does not send the phrase to DingDone's text-to-speech server or to Fish Audio.

### DingDone Premium voices

Premium voices are cloud-based. When a Premium voice is selected and DingDone speaks a
notification, the app sends:

- the short generated status phrase;
- the selected DingDone voice identifier;
- language and speed settings; and
- an opaque installation authorization token

to `tts.dingdone.io` over TLS. A typical phrase contains the coding-agent name, the project
name, and a status such as "finished" or "waiting for your response." DingDone then sends the
phrase and the provider voice settings to Fish Audio to generate the audio.

DingDone does not add source code, prompts, agent transcripts, or full agent messages to the
hosted voice request. DingDone's proxy does not store the phrase or generated notification
audio in its database and does not include the phrase or project name in server logs. It logs
limited operational metadata such as request size, DingDone voice identifier, language,
status, quota, and error category. Fish Audio processes the text and output under the
[Fish Audio Privacy Policy](https://fish.audio/privacy/).

If you do not want notification phrases processed in the cloud, select an Apple system voice.

### Optional ElevenLabs bring-your-own-key mode

Pro users may optionally enter their own ElevenLabs API key. In this mode, DingDone sends the
short phrase, voice selection, and synthesis settings directly from the Mac to ElevenLabs.
DingDone's servers do not receive the ElevenLabs key or the phrase sent in this mode.

The key is stored locally in DingDone's `config.json`, protected by filesystem permissions
for the current macOS user, rather than in the macOS Keychain. ElevenLabs processes the input
and output under the [ElevenLabs Privacy Policy](https://elevenlabs.io/privacy-policy).
Remove the key from DingDone settings when you no longer want to use this mode.

## 5. Network and operational data

Like most internet services, DingDone's licensing, support, update, and text-to-speech
infrastructure may temporarily process technical request information such as IP address,
request time, route, response status, app version, and user-agent information. We use this
information to operate the service, secure it, diagnose failures, enforce fair-use limits,
and prevent abuse.

DingDone does not use this information for targeted advertising and does not include a
third-party behavioral analytics SDK in the macOS app.

## 6. Retention

Current server-side retention defaults are:

- text-to-speech rate-limit buckets: 24 hours;
- completed background jobs and processed sanitized webhook records: 30 days;
- dead-letter jobs and safe audit records: 180 days; and
- purchase, entitlement, installation, keyed lookup, sale/subscription, and aggregated usage
  records: for as long as reasonably needed to operate the license, enforce fair-use limits,
  resolve refunds and disputes, prevent fraud, provide support, and meet legal obligations.

DingDone does not currently promise automatic deletion of purchase and entitlement records.
Requests for deletion are handled manually and may be limited where records must be retained
for security, fraud prevention, accounting, dispute resolution, or legal obligations.

The notification phrase and generated notification audio are not intentionally persisted by
DingDone's hosted voice server after the request completes. Third-party providers may apply
their own retention rules under their policies. Support emails are retained for as long as
reasonably needed to answer the request, maintain support history, and protect legal rights.
Infrastructure security logs are retained and rotated according to operational and security
needs.

## 7. Service providers

DingDone uses the following providers for the purposes described below:

- **Gumroad** — checkout, payments, receipts, refunds, subscriptions, and software license
  keys. [Privacy policy](https://gumroad.com/privacy)
- **Fish Audio** — cloud text-to-speech for DingDone Premium voices.
  [Privacy policy](https://fish.audio/privacy/)
- **ElevenLabs** — optional direct text-to-speech when you provide your own API key.
  [Privacy policy](https://elevenlabs.io/privacy-policy)
- **Webdock** — virtual-server infrastructure for DingDone's licensing and hosted voice
  services. [Legal and privacy documents](https://webdock.io/en/docs/general-information/legal-stuff)
- **Porkbun** — domain, DNS, and support-email forwarding.
  [Privacy policy](https://porkbun.com/legal/agreement/privacy_policy)
- **GitHub** — release downloads, the Sparkle update feed, and this privacy-policy page.
  [Privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement)

These providers may process information in countries other than your own. Their processing
is governed by their own terms and privacy policies.

## 8. Security

DingDone uses reasonable technical and organizational safeguards, including TLS for network
requests, macOS Keychain protection for DingDone license credentials, restricted database
roles, hashed or keyed server-side lookup values, access controls, and separation between the
license service and text-to-speech proxy.

No method of transmission or storage is completely secure. Please keep your Mac, Gumroad
license key, and any third-party API key secure.

## 9. Your choices and rights

Depending on where you live, you may have rights to request access to, correction of,
deletion of, restriction of, or an export of personal information DingDone controls. You may
also object to certain processing.

To make a request, email [support@dingdone.io](mailto:support@dingdone.io). We may need to
verify that you are the purchaser or otherwise entitled to make the request. For payment and
checkout information controlled by Gumroad, you may also need to contact Gumroad directly.

You can also:

- use Apple system voices to keep speech synthesis local;
- avoid or remove the optional ElevenLabs API key;
- deactivate a Mac from DingDone's license settings; and
- remove local history, cache, configuration, and Keychain items from your Mac.

## 10. Children

DingDone is intended for software-development workflows and is not directed to children under
13. We do not knowingly collect personal information from children under 13. If you believe a
child has provided personal information to DingDone, contact us so we can investigate and
delete it where appropriate.

## 11. Changes to this policy

We may update this Privacy Policy when DingDone's features, providers, or legal obligations
change. The effective date at the top will be updated when a new version is published.
Material changes will be communicated where required by law.

## 12. Contact

For privacy, support, or data requests, contact:
[support@dingdone.io](mailto:support@dingdone.io).
