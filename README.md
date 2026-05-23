# RCCMS Pro — Revenue Court Case Management System

> **न्यायालय केस प्रबंधन प्रणाली** — A premium PWA portal for managing revenue court cases with real-time Firebase sync.

![RCCMS Pro](https://img.shields.io/badge/RCCMS-Pro-gold?style=for-the-badge&logo=balance-scale)
![PWA](https://img.shields.io/badge/PWA-Ready-blue?style=for-the-badge)
![Firebase](https://img.shields.io/badge/Firebase-Realtime_DB-orange?style=for-the-badge&logo=firebase)

---

## 🚀 Features

- **🔐 Secure Login** — Firebase Authentication
- **📋 Case Management** — Add, manage, and dispose cases
- **📊 Statistics Dashboard** — Live stats with animated counters
- **📈 MPR Reports** — Pending & Disposal Monthly Progress Reports
- **📂 Excel Import/Export** — Bulk import cases from .xlsx files
- **💾 Backup & Restore** — JSON backup/restore
- **📱 PWA (App Install)** — Works on Android as an APK-like app
- **🌐 Offline Support** — Service Worker for basic offline access
- **⚡ Real-time Sync** — Firebase Realtime Database

---

## 📁 Project Structure

```
rccms/
├── index.html       ← Main application (all-in-one)
├── manifest.json    ← PWA manifest
├── sw.js            ← Service Worker
├── icons/           ← App icons (add your own)
│   ├── icon-192.png
│   └── icon-512.png
└── README.md
```

---

## 🌐 GitHub Pages Deployment

1. **Upload files** to your GitHub repository
2. Go to **Settings → Pages**
3. Source: **Deploy from branch → main → / (root)**
4. Your app will be live at: `https://yourusername.github.io/repo-name/`

---

## 📱 Convert to APK (Android App)

### Method 1: PWA Builder (Easiest)
1. Deploy to GitHub Pages first
2. Go to **[pwabuilder.com](https://www.pwabuilder.com)**
3. Enter your GitHub Pages URL
4. Click **Start** → **Android** → **Download Package**
5. Follow instructions to sign and publish

### Method 2: Trusted Web Activity (TWA)
```bash
npm install -g @bubblewrap/cli
bubblewrap init --manifest https://yourusername.github.io/repo-name/manifest.json
bubblewrap build
```

---

## 🔧 Firebase Setup

The app uses these Firebase services (already configured):
- **Authentication** — Email/Password login
- **Realtime Database** — Case data storage

To use your own Firebase project:
1. Create project at [console.firebase.google.com](https://console.firebase.google.com)
2. Enable **Authentication → Email/Password**
3. Enable **Realtime Database**
4. Replace `firebaseConfig` in `index.html` with your config

### Firebase Security Rules
```json
{
  "rules": {
    "rccms_cases": {
      ".read": "auth != null",
      ".write": "auth != null"
    }
  }
}
```

---

## 📊 Excel Import Format

### Cases Excel (`Import Cases`)
| Case No | Institution Date | Section | Purpose | Appellant | Respondent | Hearing Date |
|---------|-----------------|---------|---------|-----------|------------|--------------|
| 2025/001 | 01-01-2025 | 212 | साक्ष्य | Ram | Shyam | 15-06-2025 |

### Disposal Excel (`Import Disposal`)
| Case No | Disposal Date |
|---------|--------------|
| 2025/001 | 30-05-2025 |

---

## 🎨 Design

- **Theme**: Dark judicial/legal with gold accents
- **Fonts**: Playfair Display (headings) + DM Sans (body)
- **Framework**: Vanilla HTML/CSS/JS — no build step required
- **Responsive**: Works on mobile, tablet, and desktop

---

## 📞 Support

Built with Firebase + SheetJS + Font Awesome.  
All data is stored in YOUR Firebase project — private and secure.

---

*Made for Revenue Court Officers — न्यायालय अधिकारियों के लिए निर्मित* ⚖️
