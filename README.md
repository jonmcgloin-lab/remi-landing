# Remi Landing Page

Premium personal gifting platform landing page. Editorial luxury aesthetic with cream, terracotta, and deep brown palette.

## Features

- ✅ Conversion-optimized email capture
- ✅ Mobile-responsive design  
- ✅ Brand-compliant typography (Cormorant Garamond + DM Sans)
- ✅ Smooth animations and micro-interactions
- ✅ Dubai market focus with international capability

## Quick Deploy to Vercel

### Option 1: Vercel CLI (Recommended)

```bash
# Install Vercel CLI (if not already installed)
npm i -g vercel

# Login to your Vercel account
vercel login

# Deploy from this directory
vercel

# Follow prompts:
# - Link to existing project? No
# - Project name: remi-landing
# - Directory: ./  (current)
# - Deploy? Yes

# Add custom domain
vercel domains add remigft.com
```

### Option 2: Vercel Dashboard

1. Go to [vercel.com/dashboard](https://vercel.com/dashboard)
2. Click "New Project"
3. Import from Git or drag/drop these files:
   - `index.html`
   - `vercel.json` 
   - `package.json`
4. Deploy
5. Go to Project Settings → Domains → Add `remigft.com`

## Custom Domain Setup (GoDaddy)

In your GoDaddy DNS settings, add:

```
Type: CNAME
Name: www
Value: cname.vercel-dns.com

Type: A
Name: @
Value: 76.76.19.61
```

Or use Vercel nameservers for full DNS management:
```
ns1.vercel-dns.com
ns2.vercel-dns.com
```

## Email Capture Integration

Currently shows alert. To integrate with email service:

### With Mailchimp:
```javascript
// Replace the form handler in index.html
fetch('https://your-domain.us1.list-manage.com/subscribe/post-json?u=YOUR_USER_ID&id=YOUR_LIST_ID&EMAIL=' + email)
```

### With ConvertKit:
```javascript
fetch('https://api.convertkit.com/v3/forms/YOUR_FORM_ID/subscribe', {
  method: 'POST',
  headers: {'Content-Type': 'application/json'},
  body: JSON.stringify({email: email, api_key: 'YOUR_API_KEY'})
})
```

### With Vercel Serverless Function:
Create `api/subscribe.js` for backend email handling.

## Analytics

Add to `<head>` in index.html:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_TRACKING_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_TRACKING_ID');
</script>
```

## AWIN Publisher Application

Once live at remigft.com:
1. Go to [awin.com/publisher](https://www.awin.com/gb/publishers)
2. Apply with website URL: https://remigft.com
3. Category: Gift & Flowers
4. Traffic: 1000+ monthly (projected)

## Performance

- ✅ Static HTML/CSS/JS - loads in <1s
- ✅ Optimized Google Fonts loading
- ✅ Mobile-first responsive design
- ✅ SEO-friendly structure

## Brand Guidelines

**Colors:**
- Cream: #FAF7F2
- Terracotta: #C4714A  
- Deep Brown: #1C1410
- Gold: #B8965A

**Typography:**
- Display: Cormorant Garamond
- Body: DM Sans

**Voice:** Warm, considered, effortless. Like a brilliant friend with exceptional taste.
