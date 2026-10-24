# Whisper — Secret Feelings Website

## Run locally
1. Extract `whisper-website.zip`.
2. Open `index.html` in a modern browser to preview the layout.
3. For encryption, use HTTPS hosting or a local development server. Some browser security features may not work from a `file://` URL.

## Free hosting with Cloudflare Pages (static site)
1. Sign in to Cloudflare and open **Workers & Pages**.
2. Choose **Create application** → **Pages** → **Upload assets** (the wording may vary).
3. Upload the extracted folder containing `index.html`, or a ZIP if the dashboard accepts it.
4. Deploy the site and open the provided `*.pages.dev` HTTPS address.
5. Test with a non-sensitive sample message on your phone and a second browser.

## Important privacy and expiry notes
- The message is encrypted in the browser using Web Crypto (AES-GCM with a password-derived key).
- The encrypted payload is carried inside the URL fragment. It is not uploaded to a message database by this starter site.
- Send the password separately from the link. Anyone who has both can read the message.
- Expiry in this starter is a **client-side convenience**, not a tamper-proof expiry service. A recipient can potentially alter the expiry value or save the content before it expires. True server-enforced expiry/deletion requires a backend that stores messages and checks expiry server-side.
- This is a starter project, not a security-audited service. Do not use it for highly sensitive information.
