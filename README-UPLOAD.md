# Invoice Pop support site — for invoicepop.northcedarsoftware.com

These are static pages rebuilt from the current live site
(the current chatgpt.site support site) with the contact email
changed to support@northcedarsoftware.com. No content was added or removed.

## Files (upload to the ROOT of a new public GitHub repo, e.g. "invoicepop-support")

- `index.html` → https://invoicepop.northcedarsoftware.com/
- `privacy/index.html` → https://invoicepop.northcedarsoftware.com/privacy/
- `delete-account/index.html` → https://invoicepop.northcedarsoftware.com/delete-account/
- `CNAME` → tells GitHub Pages the custom domain (already filled in)

## Steps

1. Create a new **public** GitHub repo (any name) and upload these files/folders at the root.
2. Repo → Settings → Pages → "Build and deployment": Source = **Deploy from a branch**, Branch = **main** / **(root)** → Save.
3. Same Pages screen → Custom domain should show `invoicepop.northcedarsoftware.com` (read from the CNAME file) → Save.
4. In **Namecheap**: Domain List → northcedarsoftware.com → Manage → **Advanced DNS** → Add New Record:
   - Type: **CNAME Record**
   - Host: **invoicepop**
   - Value: **<your-github-username>.github.io**
   - TTL: Automatic
5. Wait for DNS (usually minutes, can take longer). GitHub shows "DNS check successful", then tick **Enforce HTTPS** (the certificate is issued automatically; can take up to ~1 hour).
6. Verify the three URLs above load, then update the privacy-policy and account-deletion links in Play Console and in the app to the new addresses.
7. Keep the old chatgpt.site pages live until the new ones are verified; retire them afterwards.

Note: the root domain (northcedarsoftware.com company page) is a separate, later step — GitHub Pages serves one custom domain per repo, so the company hub gets its own repo when needed.
