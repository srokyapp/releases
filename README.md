# Sroky releases

Android builds of Sroky that are shared outside Google Play, and the feed the app reads to offer an update.

* `latest.json`: the newest build. The app only accepts an APK from this repository's release page and only a higher build number than the one installed.
* Android installs an update only when it is signed with the same key as the installed app.
* `directory.json`: the verified lawyers and the support contacts shown in the app. A lawyer is added only after the team checked the licence on the Bar Association site (see the vault note Lawyers). The app ignores any entry that is not well formed.

To add a lawyer, add an object to `lawyers`:

```json
{
  "id": "short_unique_id",
  "name": "Full name",
  "firm": "Law office name or null",
  "city": "Baku",
  "languages": ["Azerbaijani", "English", "Russian"],
  "areas": ["residence", "business", "family", "labour", "property", "tax", "criminal"],
  "phones": [{ "display": "+994 12 000 00 00", "tel": "+994120000000" }],
  "whatsapp": "+994500000000",
  "email": "office@example.az",
  "website": "https://example.az",
  "licence": "licence number",
  "verifiedOn": "2026-10-28"
}
```

Support contacts: set `support.email` and `support.whatsapp` (as +994500000000). Changes show in the app within 6 hours, no new build needed.

Source code is private. Questions: the Sroky team.
