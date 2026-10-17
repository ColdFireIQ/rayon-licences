# Rayon licence status

`status.txt` is read by Rayon on cars with internet, every few hours. It can withdraw a
licence or move its expiry later, by licence number only: there are no VINs, VIN hashes or
names in it. It is signed with the Rayon licence key, so an edited copy is ignored by the
app, and an older list never replaces a newer one.

Made with `hu-license.ps1 -Publish`. Do not edit by hand: any change breaks the signature.

## Updates

`update.txt` announces the latest RayOn release (version, download address, SHA-256,
release notes), signed with the same key. `releases/` holds that release's APK. Cars
show a notice; nothing installs unless the driver chooses Download, then Install, and
confirms on Android's own install screen. RayOn checks the file against the notice and
that it is signed with the same certificate as the installed app before offering it.
Made with `hu-license.ps1 -PublishUpdate` (or `RayOn release`).
