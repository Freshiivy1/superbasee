# Superbrass

One page website for Superbrass: website builds, app builds and backend hosting.

## What's on the page

- **Websites:** built free for orders up to 17 Feb 2027 (launch offer), then $150 each. The page switches over by itself on that date.
- **Apps:** $300 for iPhone and Android, published to the App Store and Google Play.
- **Backend hosting:** Starter $35, Pro $71 and Team $892 a month, with the full feature list.
- A live quote calculator, a request form and Stripe checkout buttons.

All prices are in AUD.

## Deploying

The whole site is one static `index.html` with no build step. Put it on any static host (Vercel, Netlify, GitHub Pages or a zip upload) and it works as is.

## Settings

Everything you'd change is in the `CONFIG` block at the top of the script in `index.html`:

| Setting | What it does |
|---|---|
| `contactEmail` | Inbox that customer requests go to. While it's blank, the form lets people copy their request instead. |
| `formEndpoint` | Optional URL that accepts a JSON POST, if you want requests sent automatically. |
| `promoEnds` | Last day of the free website offer (Sydney time). |
| `websitePrice`, `appPrice` | Build prices in AUD. |
| `backendPlans` | Monthly backend plan prices in AUD. |
| `stripeLinks` | Stripe Payment Links for each product. |

If you change a price here, change the matching price in Stripe too, so checkout charges what the page shows.
