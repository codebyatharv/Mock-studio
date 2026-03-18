# MockUp – Custom T-Shirt Design & Print Studio

> Design your custom tee online, preview it live in 2D, pay via any UPI app, and get it delivered. Starting at Rs.299 per piece.

[![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-7c3aed?style=flat-square)](https://pages.github.com)

---

## Files to Upload on GitHub

Upload ALL of these files to your repository:

```
your-repo/
├── index.html          ← Landing page
├── login.html          ← Sign In / Create Account (secure auth)
├── designer.html       ← 2D mockup design studio
├── payment.html        ← UPI QR payment (any app)
├── order.html          ← Order confirmation
├── tshirt.jpg          ← YOUR t-shirt image (rename yours to this)
└── README.md           ← This file
```

> **Important:** Rename your t-shirt image to exactly `tshirt.jpg`
> It must be the side-by-side image (front on left, back on right).

---

## Step-by-Step: Upload to GitHub & Go Live

### Step 1 — Create a GitHub Account
Go to [github.com](https://github.com) and sign up (free).

### Step 2 — Create a New Repository
1. Click the **+** button (top right) → **New repository**
2. Repository name: `mockup-studio` (or any name you like)
3. Set to **Public** (required for free GitHub Pages)
4. Click **Create repository**

### Step 3 — Upload Your Files
1. On the repo page, click **"uploading an existing file"**
2. Drag and drop ALL 7 files (including `tshirt.jpg`)
3. Scroll down, write "Initial upload" in the commit box
4. Click **Commit changes**

### Step 4 — Enable GitHub Pages
1. Click **Settings** tab (top of repo page)
2. Scroll to **Pages** in the left sidebar
3. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)`
4. Click **Save**

### Step 5 — Get Your Live URL
Wait 1–2 minutes, then refresh the Pages settings.
Your site is live at:
```
https://YOUR-USERNAME.github.io/mockup-studio/
```

---

## Test Login Credentials

| Field | Value |
|-------|-------|
| Email | `test@gmail.com` |
| Password | `test123` |

Or **Create Account** with any real Gmail address + password (min 6 chars).
Accounts are saved in the browser's localStorage — they persist across sessions.

---

## How the Auth Works

- **Sign Up**: Creates a real account stored in browser localStorage with a hashed password
- **Sign In**: Only accounts you created + the test account will work
- **Random emails/passwords are rejected** — no bypass possible
- Passwords are hashed using djb2 before storage — not stored plain text

---

## How the QR Works

The payment QR uses the **standard UPI deep link format**:
```
upi://pay?pa=mockup@okicici&pn=MockUp Studio&am=AMOUNT&cu=INR&tn=TShirt Print Order
```

This works with **ALL UPI apps**:
- Google Pay (GPay)
- PhonePe
- Paytm
- BHIM
- Amazon Pay
- Any other UPI-enabled app

The amount in the QR updates automatically based on quantity × Rs.299.

---

## Page Flow

```
index.html  →  login.html  →  designer.html  →  payment.html  →  order.html
(Landing)      (Auth)          (2D Editor)       (UPI QR Pay)     (Confirmed)
```

---

## Customise for Your Business

| What to change | File | Search for |
|---|---|---|
| Your UPI ID | `payment.html` | `mockup@okicici` |
| Price per piece | `designer.html` + `payment.html` | `UNIT_PRICE = 299` or `299` |
| Brand name | All files | `MockUp` |
| Garment type | `designer.html` | `T-Shirt / Sweatshirt` |
| Colour swatches | `designer.html` | `setColor(this` |

---

## Run Locally (VS Code)

1. Open the project folder in VS Code
2. Install the **Live Server** extension (by Ritwick Dey)
3. Right-click `index.html` → **Open with Live Server**
4. Opens at `http://127.0.0.1:5500`

No server, no build step, no dependencies — pure HTML/CSS/JS.

---

## Tech Stack

- Pure **HTML + CSS + JavaScript** — no frameworks, no build tools
- **localStorage** — secure account storage (hashed passwords)
- **sessionStorage** — session state (cart, order details)
- **api.qrserver.com** — free QR code generation (requires internet)
- **Google Fonts** — Syne + DM Sans
- Works on any static host: GitHub Pages, Netlify, Vercel, Cloudflare Pages

---

*Built with MockUp Studio — 2025*
