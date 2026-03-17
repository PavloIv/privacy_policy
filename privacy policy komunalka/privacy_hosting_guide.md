# Hosting Guide for Privacy Policy (Google Play)

Use one of these options to get a public URL for Play Console.

## Option A: GitHub Pages (fastest)

1. Create a public repo (or use your existing public repo).
2. Upload these files from `/docs`:
   - `privacy_index.html`
   - `privacy_policy_uk.html`
   - `privacy_policy_en.html`
3. In GitHub repo settings:
   - `Settings` -> `Pages`
   - `Build and deployment` -> `Deploy from a branch`
   - choose branch (`main`) and folder (`/docs` or `/root`)
4. Save and wait 1–3 minutes.
5. You will get URL like:
   - `https://<username>.github.io/<repo>/privacy_index.html`
6. Put this URL into Play Console -> Privacy Policy.

## Option B: Firebase Hosting

1. Install CLI:
```bash
npm i -g firebase-tools
```

2. Login:
```bash
firebase login
```

3. Init hosting in project root:
```bash
firebase init hosting
```

Recommended answers:
- Use existing Firebase project: `komunalka-ce4b4`
- Public directory: `docs`
- Single-page app rewrites: `No`
- Overwrite `index.html`: `No`

4. Deploy:
```bash
firebase deploy --only hosting
```

5. Use URL:
- `https://<project-id>.web.app/privacy_index.html`

## What URL to use in Play Console

Best choice:
- `.../privacy_index.html` (language selector page)

Direct language URL is also valid:
- `.../privacy_policy_uk.html`
- `.../privacy_policy_en.html`
