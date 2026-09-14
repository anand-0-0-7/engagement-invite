# 💍 Indian Engagement Ceremony — Web Invitation

A premium, animated, single-page web invitation for an Indian engagement ceremony. Mobile-first, WhatsApp-optimized, and ready to deploy.

---

## ✨ Features

- 💌 **Interactive Envelope** — 3D animated digital envelope that opens to reveal the invitation.
- 🔮 **Glassmorphism UI** — Frosted glass effects on the event details and countdown cards.
- 🌸 **Canvas Falling Petals** — Smooth, physics-based canvas animation of falling pastel petals.
- 🗓️ **Add to Calendar** — Google Calendar template link so guests can save the date in one tap.
- 🌿 **Botanical Elements** — Elegant SVG botanical line art floating in the background.
- 📱 **100% Mobile Responsive** — Optimized for phones.
- 🔗 **WhatsApp OG Tags** — Beautiful link preview when shared on WhatsApp.
- 🎵 **Background Music** — Plays when the envelope is opened.
- ⏳ **Live Countdown Timer** — Ticks down to the event date.
- 📍 **Google Maps Link** — Direct venue directions.
- 💬 **WhatsApp RSVP** — One-tap reply button.

---

## 🎯 Quick Customization Guide

Open `index.html` and search for `CUSTOMIZE` to find all placeholders. Here's what to change:

### 1. **Couple Names**
```html
Priya → [Your Bride's Name]
Rahul → [Your Groom's Name]
```

### 2. **Event Date, Time, Venue**
```html
Sunday, 15th November 2026  → [Your Date]
6:00 PM onwards             → [Your Time]
The Grand Palace Banquet Hall → [Your Venue Name & Address]
```

### 3. **Countdown Target Date** (in JavaScript)
```javascript
const EVENT_DATE = new Date(2026, 10, 15, 18, 0, 0);
// Format: new Date(YEAR, MONTH-1, DAY, HOUR, MINUTE, 0)
// Month is 0-indexed: 0=Jan, 1=Feb, ..., 10=Nov
```

### 4. **Family Names**
Replace the placeholder names for both bride's and groom's families.

### 5. **Couple Photo**
```html
<!-- Uncomment and replace: -->
<img class="couple__photo" src="assets/couple-photo.jpg" alt="Bride & Groom" />
<!-- Remove the placeholder div -->
```

### 6. **Google Maps Link**
```html
href="https://maps.google.com/?q=28.5355,77.3910"
```

### 7. **WhatsApp RSVP**
```html
href="https://wa.me/919876543210?text=..."
```

### 8. **Background Music**
Place your shehnai/sitar MP3 in `assets/music.mp3`.
Free sources:
- [Pixabay - Indian Music](https://pixabay.com/music/search/indian/)
- [Free Music Archive](https://freemusicarchive.org/)

### 9. **OG Meta Tags** (after deployment)
```html
<meta property="og:image" content="https://your-site.netlify.app/assets/og-preview.jpg" />
<meta property="og:url" content="https://your-site.netlify.app/" />
```

---

## 🚀 3-Step Free Deployment Guide

### Option A: **GitHub Pages** (Easiest)

1. **Create a GitHub repo:**
   ```bash
   git init
   git add .
   git commit -m "Engagement invitation"
   git remote add origin https://github.com/YOUR_USERNAME/engagement-invite.git
   git push -u origin main
   ```

2. **Enable GitHub Pages:**
   - Go to your repo → **Settings** → **Pages**
   - Source: **Deploy from a branch**
   - Branch: `main`, Folder: `/ (root)`
   - Click **Save**

3. **Share your link:**
   ```
   https://YOUR_USERNAME.github.io/engagement-invite/
   ```

---

### Option B: **Netlify** (Drag & Drop)

1. **Go to [netlify.com](https://app.netlify.com/drop)** and sign up (free).

2. **Drag & drop** the entire `InvitationCard` folder onto the Netlify dashboard.

3. **Copy your link** — Netlify gives you a URL like `https://random-name.netlify.app`. You can customize it in Site Settings.

---

### Option C: **Vercel** (CLI)

1. **Install Vercel CLI:**
   ```bash
   npm i -g vercel
   ```

2. **Deploy:**
   ```bash
   cd InvitationCard
   vercel --prod
   ```

3. **Share the link** Vercel provides.

---

## 📁 File Structure

```
InvitationCard/
├── index.html              ← Main invitation
├── assets/
│   ├── og-preview.jpg      ← WhatsApp link preview image (1200×630)
│   ├── music.mp3           ← Your shehnai/sitar audio (add your own)
│   └── couple-photo.jpg    ← Your couple photo (add your own)
└── README.md               ← This file
```

---

## ⚠️ Important Notes

- **OG Image URL must be absolute** — After deployment, update the `og:image` meta tag in `index.html` with your full URL.
- **WhatsApp caches OG data** — If the preview doesn't show, use [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/) to refresh the cache.
- **Music file** — Add your own `assets/music.mp3`. The invitation works fine without it too.
- **Couple photo** — For best results, use a square photo (at least 500×500px).
