# Rayon licence status

`status.txt` is read by Rayon on cars with internet, every few hours. It can withdraw a
licence or move its expiry later, by licence number only: there are no VINs, VIN hashes or
names in it. It is signed with the Rayon licence key, so an edited copy is ignored by the
app, and an older list never replaces a newer one.

Made with `hu-license.ps1 -Publish`. Do not edit by hand: any change breaks the signature.
