# 📚 LibraryOS — Mobile App (PWA)

A fully installable Progressive Web App (PWA) for managing libraries,
fixed seats, and monthly fee tracking.

---

## 📲 Install as App (Recommended)

### Android (Chrome)
1. Open `index.html` in Chrome
2. Tap the **"Install"** banner that appears at the top
   — OR — tap the 3-dot menu → "Add to Home Screen"
3. Done! Tap the LibraryOS icon on your home screen

### iPhone / iPad (Safari)
1. Open `index.html` in Safari
2. Tap the **Share** button (□↑)
3. Tap **"Add to Home Screen"**
4. Tap **Add** — the app icon will appear

### Desktop (Chrome / Edge)
1. Open `index.html` in Chrome or Edge
2. Click the install icon (⊕) in the address bar
3. Click **Install**

---

## 🖥️ Open Without Installing
Just double-click `index.html` — it opens in your browser.
Works offline too, after first load.

---

## ✨ What's New vs Previous Version

### 🐛 Vacant Seat Bug — FIXED
- Vacating a seat now **immediately** marks it as empty
- The seat map and empty seats list update **instantly**
- Added a **race-condition guard**: if two users try to assign
  the same seat simultaneously, the second gets a warning
- All seat checks now use `active === true` (strict check)

### 📱 Mobile App Features
- Installable on Android, iPhone & Desktop (PWA)
- Splash screen on launch
- Bottom navigation bar (Seats / Students / Empty / Fees)
- Library tabs at the top — scroll if many libraries
- Bottom sheets instead of centered modals
- Touch-optimized seat grid
- Student search bar
- Safe area support (iPhone notch / Dynamic Island)
- Works fully **offline** after first load

---

## 🚀 How to Use

1. **Add a Library** — tap "+ Library" in top-right
   (Name, seat count, monthly fee, location)

2. **Seat Map** — visual color-coded grid
   - 🔲 Gray = Empty (tap to assign student)
   - 🟩 Green = Occupied + fee paid
   - 🟥 Red = Occupied + fee unpaid

3. **Register Student** — tap any empty seat
   Fill name, phone, join date, course
   Option to mark first month as paid

4. **Fee Tracking**
   - Tap occupied seat → "Mark Fee as Paid"
   - Fee Report tab shows collected vs pending per month

5. **Vacate Seat** — tap occupied seat → "Vacate"
   Confirm → seat instantly becomes empty and reassignable

---

## 💾 Data Storage
All data saves in your browser's **localStorage** automatically.
Persists between sessions on the same browser/device.

---

## 📁 Files
```
LibraryOS-App/
├── index.html      ← Main app (open this)
├── manifest.json   ← PWA install config
├── sw.js           ← Offline service worker
├── icon-192.png    ← App icon (small)
├── icon-512.png    ← App icon (large)
└── README.md       ← This file
```
