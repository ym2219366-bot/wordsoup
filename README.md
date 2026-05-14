# Descifrador 🐱 — Spanish Word Unscrambler

## Files in this package
```
descifrador/
├── index.html          ← Main tool (homepage)
├── sitemap.xml         ← Submit to Google Search Console
├── robots.txt          ← Search engine instructions
├── vercel.json         ← Vercel deployment config (clean URLs)
└── pages/
    ├── about.html      ← About page (AdSense requirement)
    ├── contact.html    ← Contact page (AdSense requirement)
    ├── privacy.html    ← Privacy Policy (AdSense requirement)
    ├── blog.html       ← Blog index (SEO + AdSense)
    └── word-lists.html ← Word lists (SEO traffic)
```

---

## Launch checklist (do this today)

### Step 1 — Domain (~10 min)
1. Go to namecheap.com or cloudflare.com/registrar
2. Register: sopadepalabras.com (or similar — check availability)
3. Cost: ~$10/year

### Step 2 — GitHub (~5 min)
1. Create a new GitHub repo (e.g. `sopadepalabras`)
2. Upload all files from this package, preserving folder structure
3. Make repo public

### Step 3 — Vercel deploy (~10 min)
1. Go to vercel.com → New Project
2. Import your GitHub repo
3. Click Deploy (zero config needed — vercel.json handles routing)
4. Go to Settings → Domains → Add your domain
5. Point your domain nameservers to Vercel (instructions provided in Vercel dashboard)

### Step 4 — Add your Anthropic API key
In index.html, the fetch call to api.anthropic.com is already set up.
You need to handle API key auth server-side for production.
Options:
- Vercel Edge Function (recommended): create /api/unscramble.js as a proxy
- Or use a Cloudflare Worker
- Never expose your API key in client-side code

### Step 5 — Google Analytics (~10 min)
1. Go to analytics.google.com → Create Property
2. Get your Measurement ID (G-XXXXXXXXXX)
3. Uncomment and update the GA4 script tag in index.html
4. Repeat for all pages

### Step 6 — Google Search Console (~5 min)
1. Go to search.google.com/search-console
2. Add property → enter your domain
3. Verify ownership (easiest: add DNS TXT record in Cloudflare/Namecheap)
4. Submit sitemap: https://yourdomain.com/sitemap.xml

---

## AdSense setup (do after 2 weeks + some traffic)

1. Apply at google.com/adsense
2. All 3 required pages are already built: About, Privacy, Contact
3. Once approved, replace all `<div class="ad-slot ...">` placeholders with real AdSense code
4. Enable Auto Ads first, then add manual placements

### Ad slot locations already in the code:
- **Top of page**: 728×90 leaderboard (desktop) / 320×50 (mobile)
- **Sidebar**: 300×250 rectangle
- **In-results**: injected between word-length groups
- **Mid-content**: 728×90 between features and email section
- **Bottom**: 728×90 footer leaderboard
- **Blog pages**: in-article ads between posts

---

## Affiliate links to replace

In index.html sidebar, replace these URLs with your actual affiliate links:
- Babbel: apply at babbel.com/affiliates (pays ~$20-40/conversion)
- Rosetta Stone: apply at rosettastone.com (pays ~$10-20/conversion)  
- Pimsleur: apply at pimsleur.com/affiliates (pays ~$15-30/conversion)

---

## Newsletter setup

The email form in index.html currently shows a success message only.
To actually collect emails:
1. Create a free account at Mailchimp, ConvertKit, or Beehiiv
2. Get your form embed code
3. Replace the handleSignup() function with their API endpoint
4. Set up a welcome email sequence mentioning the cat litter table cover early access

---

## Cat Litter Table Cover — product teaser

The sidebar card and email CTA already promote the product launch.
When ready:
1. Update the "Coming Soon" badge to "Now Available"
2. Replace the "#newsletter" link with your product page URL
3. Add product photos to the sidebar card
4. Send a dedicated email to your list on launch day

---

## SEO content calendar (weeks 1-8)

### Publish 2 posts/week to /pages/blog/
Week 1: "100 most useful 5-letter Spanish words" + "Spanish words with Q"
Week 2: "How word games build fluency" + "Spanish words with Ñ complete guide"
Week 3: "50 common 3-letter Spanish words" + "How to solve Spanish crosswords"
Week 4: "Spanish Scrabble tips" + "Words ending in -ción"
Week 5: "Spanish words starting with X" + "Common Spanish verb forms for word games"
Week 6: "Spanish Wordle strategy" + "Animal words in Spanish"
Week 7: "Food words in Spanish for Scrabble" + "Body parts in Spanish word games"
Week 8: "Best Spanish word game apps" (affiliate opportunity) + "Spanish color words"

---

## Revenue projections

| Month | Daily Visitors | Est. Monthly Revenue |
|-------|---------------|---------------------|
| 1     | 50–150        | $0–$15 (pre-AdSense)|
| 2     | 200–500       | $15–$60             |
| 3     | 500–1,500     | $50–$180            |
| 4     | 1,500–3,000   | $150–$400           |
| 6     | 3,000–8,000   | $300–$1,000         |

Revenue = AdSense + Affiliate commissions + Newsletter sponsorships

---

## Support
El Gato: hola@descifrador.com (he doesn't reply, but his human does)
