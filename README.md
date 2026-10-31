# SOS Directory

Local Emergency & Service Directory for Sri Lanka. Installable web app (works on iPhone and Android), offline-capable.

## Features
- One-tap call: 119 Police, 1990 Ambulance, 110 Fire & Rescue, plus other service numbers
- SOS: share your location by WhatsApp / SMS to your saved family contacts
- Nearby doctors, hospitals, pharmacies, garages, tow trucks, fuel, tyre shops (opens Google Maps)
- English / Sinhala / Tamil
- Family contacts and your own contacts (saved on the device only)
- First aid and vehicle breakdown quick guides

## Put it on GitHub Pages
1. Create a new GitHub repository (for example `sos-directory`) and upload all files in this folder.
2. Repository **Settings > Pages > Build and deployment**: Source = "Deploy from a branch", Branch = `main`, folder = `/ (root)`. Save.
3. After a minute your app is at `https://<your-username>.github.io/sos-directory/`.
4. Open that link on the phone and use Add to Home Screen. The icon and name now come from this app.

## Release an update
Edit `index.html`, change `CACHE = "sos-directory-v1"` in `sw.js` to `v2`, commit. Users get the new version next time they open it online.

## Test checklist (do on a real iPhone and a real Android phone)
- [ ] Home screen icon and name are correct after Add to Home Screen
- [ ] 119 / 1990 / 110 buttons open the dialer with the right number
- [ ] "Use my location" asks permission, then Doctors / Garage etc. open Google Maps around you
- [ ] SOS button: message contains a working maps link; WhatsApp opens with text; SMS opens to the saved numbers
- [ ] SMS with no saved family contacts still opens a message
- [ ] Add a family contact (0771234567): Call works, WA opens the correct WhatsApp chat
- [ ] Add your own contact in a category: it appears in that tab and after reload
- [ ] Delete a contact works
- [ ] Search finds items from every tab
- [ ] Language switch EN / සිං / த changes all labels and is remembered after reload
- [ ] Turn on airplane mode, reopen the app: the numbers still show (offline)
- [ ] Dark mode and light mode both readable; large text size in phone settings still usable
- [ ] Location denied: app still works and says so

## Known limits
- Nearby doctors/garages and their phone numbers come from Google Maps itself (no API key, no live data inside the app).
- Emergency numbers must be verified against official Sri Lankan sources before public release.
- First aid and breakdown text is English only. Sinhala/Tamil labels should be checked by native speakers.
- `tel:` and `sms:` links do not work on desktop browsers.
